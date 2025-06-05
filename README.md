<h1>To train cross-lingual word embeddings</h1>
<h3>https://github.com/facebookresearch/MUSE/tree/3159355b93f5c3c4883808ba785ba9d18d7f5e81</h3>

<ul>

<li>Flow of Project</li>

![image](https://github.com/user-attachments/assets/3d2186b4-20c7-437e-b37f-da6d064c668d)


<li>Approach to train Word Embeddings</li>
  <ul>
    <li>Adversarial Approach</li>
    <ul>
        <li>X is the source language, Y is the target language, and W is the rotation matrix.</li>
        <li>Using Adversarial learning, we learn a rotation matrix W.</li>
        <li>We have two functions: discriminator and mapping. Discriminator tries to discriminate between W*X and Y. While mapping prevents the discriminator from doing so.</li>
    </ul>
    <table>
      <tr>
        <td>
          <img src="https://github.com/user-attachments/assets/5432e80a-eb84-4545-b11e-3c69c2253e38">
        </td>
        <td>
          <img src="https://github.com/user-attachments/assets/104ed08b-f2a9-4573-9290-bdbe27907142">
        </td>
      </tr>
    </table>
    <li>Procrustes refinement</li>
    <ul>
        <li>The mapping W is further refined via Procrustes.</li>
        <li>Here it uses frequent words aligned by the adversarial training as anchor points.</li>
        <li>The refined mapping is then used to map all words in the dictionary.</li>
    </ul>
    <table>
      <tr>
        <td>
          <img src="https://github.com/user-attachments/assets/f8d4fd91-01eb-49d4-b899-2d9c3c917dc1">
        </td>
        <td>
          <img src="https://github.com/user-attachments/assets/c529cf8e-b94b-4615-8e6e-07b3bcf745ee">
        </td>
      </tr>
    </table>
    
  </ul>
    
<li>Visualization</li>
<img src="https://github.com/user-attachments/assets/8e18c6e7-5084-407d-8b93-de7663fbc1c2">
 
<li>Results</li>
<img src="https://github.com/user-attachments/assets/f2b1e1e7-0362-403c-b3a4-5519a2411ed7">
</ul>

