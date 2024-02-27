## Highlights

### Circle STARKs

Traditional STARKs require a cyclic group of a smooth order in the field. This allows efficient interpolation of points using the FFT algorithm, and writing constraints that involve neighboring rows. The Elliptic Curve FFT (ECFFT, Part I and II) introduced a way to make efficient STARKs for any finite field, by using a cyclic group of an elliptic curve. 

传统的STARKs需要在域中具有平滑阶数的循环群。这样可以使用FFT算法高效地插值点，并编写涉及相邻行的约束条件。椭圆曲线FFT（ECFFT，第一部分和第二部分）引入了一种使用椭圆曲线的循环群来制作任何有限域的高效STARKs的方法。

We show a simpler construction in the lines of ECFFT over the circle curve $x^2 + y^2 = 1$
. When $p+1$ 
 is divisible by a large power of 2
, this construction is as efficient as traditional STARKs and ECFFT.  Applied to the Mersenne prime 
$p=2^{31}-1$, our preliminary benchmarks indicate a speed-up by a factor of $1.4$
 compared to a traditional STARK using the Babybear prime 
.

我们在椭圆曲线 $x^2 + y^2 = 1$ 上展示了一种更简单的构造方法。当 
  $p+1$ 可被 
 的一个大幂整除时，这种构造与传统的STARKs和ECFFT一样高效。当使用了Mersenne素数 $p=2^{31}-1$ 
 ，我们的初步基准测试表明与使用Babybear素数 
 的传统STARK相比，速度提升了 1.4
 倍。

- [Paper](https://eprint.iacr.org/2024/278)


### ZKP2P

这个项目来源第312期的Zero Knowledge Podcast， 这个项目利用了Venmo的支付确认邮件的DKIM签名，用来证明SHA256、电子邮件正则表达式和RSA。这里有趣的地方在于他们利用正则表达式提取出关注的数据片段（价格），并用 zk regex 证明这个数据片段在那封来自venmo的电子邮件中。

- [zkp2p github](https://github.com/zkp2p/zk-p2p)

- [zk podcast 312](https://zeroknowledge.fm/312-2/)


### SP1 Reth

SP1 Reth是一个100%开源的POC，展示了Rollup 方案如何使用SP1构建一个高性能（type-1, bytecode compatible）的zkEVM，只需不到2000行可维护的Rust代码。通过利用SP1的开源、可定制的预编译系统，SP1 Reth实现了难以置信的性能（平均以太坊交易的证明成本约为0.01-0.02美元），未来还将有数量级的改进。

![benchamrk](https://blog.succinct.xyz/content/images/size/w1600/2024/02/FINALBENCHMARKS.png)

- [sp1 reth blog](https://blog.succinct.xyz/sp1-reth/)
- [github](https://github.com/succinctlabs/sp1-reth)


### ZKBank

zkBank 是 zkSecurity的 David 发布的基于gnark框架的一个 challenge。以下是挑战地址和内容

> Alice is a sneaky one, she's been trying to send more than what she has to Bob's account. Good thing that we use zero-knowledge proof to enforce the integrity of our transfer. We just want to make sure that Bob can get 100,000 worth of coins or more. Can you help us verify Alice's proof?

[github](https://github.com/zksecurity/zkBank)


