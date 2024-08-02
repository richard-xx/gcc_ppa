# Gcc PPA

![GitHub repo size](https://img.shields.io/github/repo-size/richard-xx/gcc_ppa) ![GitHub contributors](https://img.shields.io/github/contributors/richard-xx/gcc_ppa)

## Contains

<details>
  <summary>
    packages
  </summary>
  <ul>
    <li>
      <p>gcc-10</p>
    </li>
    <li>
      <p>gcc-11</p>
    </li>
    <li>
      <p>gcc-12</p>
    </li>
    <li>
      <p>gcc-13</p>
    </li>
    <li>
      <p>gcc-14</p>
    </li>
  </ul>
</details>

<details>
  <summary>
    Supports
  </summary>
  <ul>
    <li>
      <p>Ubuntu 16.04 + </p>
    </li>
  </ul>
</details>

## Installation

+ ### Add GPG Key

    ```shell
    sudo mkdir -p /usr/local/share/keyrings
    curl -fsSL https://richard-xx.github.io/gcc_ppa/PUBLIC.KEY \
    | gpg --dearmor \
    | sudo tee /usr/local/share/keyrings/gcc_ppa.gpg > /dev/null
    ```

+ ### Stable Gcc

    ```shell
    echo "deb [signed-by=/usr/local/share/keyrings/gcc_ppa.gpg] https://richard-xx.github.io/gcc_ppa linux main" \
    | sudo tee /etc/apt/sources.list.d/gcc_ppa.list
    sudo apt update
    sudo apt install gcc-${version}
    ```


+ ### List versions

    ```
    apt show -a "gcc-*"
    ```
