---
title: "VASP-like"
date: 2022-11-24 11:44:18
draft: True
---

# Link with this topic
1.  [markdown_list](https://markdown.com.cn/cheat-sheet.html#%E5%9F%BA%E6%9C%AC%E8%AF%AD%E6%B3%95)
2. [pymatgen](https://www.jianshu.com/p/48ef2577ca22)
3. [p4vasp](https://www.vasp.at/py4vasp/latest/)
4. [vasp_md](https://www.vasp.at/tutorials/latest/md/part1/)
5. [vaspy](https://pytlab.github.io/2016/11/26/%E4%BD%BF%E7%94%A8VASPy%E5%BF%AB%E9%80%9F%E5%A4%84%E7%90%86VASP%E6%96%87%E4%BB%B6%E4%BB%A5%E5%8F%8A%E6%95%B0%E6%8D%AE%E5%8F%AF%E8%A7%86%E5%8C%96/)

---

# Recurrent vasp_md_si
## At first, softwares prepared
1. pymatgen
2. py4vasp
3. vaspy
4. gnuplot

## pymatgen
`pip install pymatgen #failed`
### Use code below:
`module avail`
`module load conda`

### Unload envs


``` 
    module unload conda
    conda create -n my_pymatgen python # 创建虚拟环境my_pymatgen
    source activate my_pymatgen  # 激活虚拟环境
    conda install --channel conda-forge pymatgen
```

### Exit the activated env:

```
    conda deactivate my_pymatgen
    conda install gcc   # 安装gcc编译器用来编译pymatgen,已有gcc环境的不要做
```
### Update pymatgen
`conda upgrade pymatgen `

### Dependent base

`pmg config --install enumlib `
- failed when git clone, new way:

```

    git clone --recursive https://github.com/msg-byu/enumlib.git
    conda install --channel matsci enumlib #compile
```

- bader install

    `pmg config --install bader`

---

## p4vasp
```

    conda install -c conda-forge mdtraj
    pip install py4vasp
```
- Quick start
```
    from py4vasp import Calculation
    calc = Calculation.from_path(".")
```
- py4vasp is only for vaspout.h5 file

---

## vaspy
`pip install vaspy`
- how to use it
```

    from vaspy.incar import InCar
    incar = InCar("INCAR")
    incar.IBRION
    incar.ISIF = 3
```

---

## gnuplot
- First shfit to root avail

    `su`
- Enter with your password

    `yum install gnuplot`

    `gnuplot`
