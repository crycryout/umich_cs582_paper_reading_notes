read date: 2024.9.5
## philosophy of design
#### the MIT approach: phrase the right thing
Simplicity -- the design must be simple, both in implementation and interface. It is more important for the interface to be simple than the implementation
Correctness -- the design must be correct in all observable aspects. Incorrectness is simply not allowed.
Consistency -- the design must not be inconsistent. A design is allowed to be slightly less simple and less complete to avoid inconsistency. Consistency is as important as correctness.
Completeness -- the design must cover as many important situations as is practical. All reasonably expected cases must be covered. Simplicity is not allowed to overly reduce completeness.

I think in this approach, the simplicity is the least important thing, especially the simplicity of the implementation, every thing can sacrifice simplicity of implementation,such
as the simplicity of interface , the correctness that must be achieved, the consistency that is more important than complete and is at least as important as correctness.and also the completeness that can not be overly reduced for simplicity.

also, based on the above explaination, I think the priorities would be: correctness&consistency > completeness > simplicity of interface > simplicity of implementation.

#### New Jersey approach: worse is better
Simplicity -- the design must be simple, both in implementation and interface. It is more important for the implementation to be simple than the interface. Simplicity is the most important consideration in a design.
Correctness -- the design must be correct in all observable aspects. It is slightly better to be simple than correct.
Consistency -- the design must not be overly inconsistent. Consistency can be sacrificed for simplicity in some cases, but it is better to drop those parts of the design that deal with less common circumstances than to introduce either implementational complexity or inconsistency.
Completeness -- the design must cover as many important situations as is practical. All reasonably expected cases should be covered. Completeness can be sacrificed in favor of any other quality. In fact, completeness must be sacrificed whenever implementation simplicity is jeopardized. Consistency can be sacrificed to achieve completeness if simplicity is retained; especially worthless is consistency of interface.

I think this approach has put the simplicity of implementation at the most priority. To get to it, every other characteristics can be compromised:
The simplicity of interface? no, the implementation must be simplicity!
The correctness? "It is slightly better to be simple than correct."
consistency? this is always be sacrificed when it is in conflict to others.

this isn't to say other characteristics aren't important. But is we shouldn't sacrifice simplicity to achieve the most amount of these.
also, based on the above explaination, I think the priorities would be: simplicity > correctness > completeness > consistency.

## PC loser-ing

MIT choose the simplicity of interface and New Jersey choose the simplicity of implementation. clearly that to store the state of pc and program could be complex and just returning an error code would be relatively very easy to implement.
also, the user could check the code and use loop easily which New Jersey guy think is a good trade off. And the design philosophy is of Unix is to be simple and storing the state just affends this principle.

### Unix and C
one part I don't quit understand is :"the worse-is-better philosophy means that implementation simplicity has highest priority, which means Unix and C are easy to port on such machines. Therefore, one expects that if the 50% functionality Unix and C support is satisfactory, they will start to appear everywhere."

why does worth-is-better can lead to easy-to-port?
I think one explaination would be: since the implementation is easy, the instructions of hardware would be easy and resource used would be small, so most of the computer either powerful or not can all achive the requirement.

A further benefit of the worse-is-better philosophy is that the programmer is conditioned to sacrifice some safety, convenience, and hassle to get good performance and modest resource use. Programs written using the New Jersey approach will work well both in small machines and large ones, and the code will be portable because it is written on top of a virus.

Therefore, the worse-is-better software first will gain acceptance, second will condition its users to expect less, and third will be improved to a point that is almost the right thing. In concrete terms, even though Lisp compilers in 1987 were about as good as C compilers, there are many more compiler experts who want to make C compilers better than want to make Lisp compilers better.


