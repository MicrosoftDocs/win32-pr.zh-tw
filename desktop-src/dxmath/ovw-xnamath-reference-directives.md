---
description: 編譯器指示詞會微調 DirectXMath 程式庫所使用的功能。
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: DirectXMath 程式庫編譯器指示詞
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da7419afbab80d35feea135a25f7c5892b137a08
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826773"
---
# <a name="directxmath-library-compiler-directives"></a>DirectXMath 程式庫編譯器指示詞

編譯器指示詞會微調 DirectXMath 程式庫所使用的功能。



| 指示詞                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ 無 \_ 內建函式\_        | 如果 \_ \_ 沒有 \_ \_ 定義任何內建函式，則會在不使用任何平臺特定內建函式的情況下，執行 DirectXMath 作業。 相反地，DirectXMath 只會使用標準的浮點運算。<br/> 依預設， \_ \_ \_ \_ 未定義非內建函式。<br/> 這個指示詞會覆寫所有其他指示詞。 因此，建議您先檢查 [無內建]， \_ \_ \_ \_ 再判斷 [ \_ xm \_ ARM 霓虹燈] \_ \_ 內建函式 \_ 或 \_ \_ SSE SSE \_ 內建函式 \_ 的狀態。<br/>                                                                              |
| \_XM \_ SSE \_ 內建函式\_       | 當 \_ \_ \_ 定義了 XM SSE 內建函式時，程式 \_ 代碼會編譯成在支援這些指令集的平臺上使用支援 SSE 和 SSE2。<br/> 提供 SSE 內建函式的 Windows 版本支援 SSE 和 SSE2。<br/> \_\_Sse SSE \_ 內建函式不 \_ 會影響不支援 SSE 和 SSE2 的系統。<br/> 根據預設， \_ \_ \_ \_ 當使用者針對 Windows 平臺進行編譯時，會定義 XM SSE 內建函式。<br/> DirectXMath 使用標準編譯器定義 (\_ M \_ IX86/ \_ M \_ AMD64) 來判斷 windows x86 或 windows x64 目標。<br/> |
| \_XM \_ ARM \_ 霓虹燈 \_ 內建函式\_ | 這表示 DirectXMath 的執行是使用 ARM 霓虹燈內建函式。 根據預設， \_ \_ \_ \_ \_ 當使用者針對 ARM/ARM64 平臺上的 Windows 進行編譯時，會定義 XM ARM 霓虹燈內建函式。 DirectXMath 會使用標準編譯器定義 (\_ m \_ ARM、 \_ m \_ ARM64) 來判斷這個二進位目標。<br/> ARM-霓虹燈內建支援是 DirectXMath 的新功能，XNAMath 2.x 並不支援。<br/>                                                                                                                                                                             |
| \_XM \_ SSE3 \_ 內建函式\_      | DirectXMath 3.10 的新。 <br/> 當您指定這個編譯器指示詞時，DirectXMath 函式會實作為在適用的情況下使用 SSE3 內建函式;否則會使用 SSE/SSE2。<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_XM \_ SSE4 \_ 內建函式\_      | DirectMath 3.09 的新。 <br/> 當您指定這個編譯器指示詞時，DirectXMath 函式會實作為使用 SSE3 和 SSE 4.1 內建函式（如果適用）;否則會使用 SSE/SSE2。 當您指定這個編譯器指示詞時，它也會暗示 \_ \_ SSE3 \_ 內建函式 \_ 和 \_ xm \_ SSE \_ 內建函式 \_ 。<br/>                                                                                                                                                                                                                                |
| \_XM \_ AVX \_ 內建函式\_       | DirectXMath 3.09 的新。 <br/> 使用/arch： AVX 將會啟用此指示詞。 <br/> 當您指定這個編譯器指示詞時，DirectXMath 函式會實作為在適用的情況下使用 SSE3、SSE 4.1 和 AVX 128 位內建函式;否則 DirectXMath 會使用 SSE/SSE2。 當您指定這個編譯器指示詞時，它也會暗示 \_ \_ SSE3 \_ 內建函式、 \_ xm SSE4 內建 \_ \_ \_ 和 \_ xm \_ SSE \_ 內建函式， \_ 並包含一小部分的 SSE3 指令。 <br/>                                                                    |
| XM \_ AVX2 \_ 內建函式\_        | DirectXMath 3.11 的新。 <br/> 使用/arch： AVX2 可啟用此指示詞。 當您指定這個編譯器指示詞時，DirectXMath 函式會在適用的情況下使用 AVX2、F16C/CVT16、FMA3、AVX 128 位、SSE 4.1 和 SSE3 內建函式。 當您使用 \_ xm \_ AVX2 \_ 內建函式時 \_ ，它會隱含的是 [xm F16C 內建] \_ 、[ \_ \_ \_ \_ xm \_ FMA3 \_ 內建函式]、[xm AVX 內建] \_ 、[ \_ \_ \_ \_ \_ xm SSE 內建函式]、[ \_ \_ \_ \_ xm \_ SSE3 \_ \_ \_ \_ \_ \_ 內<br/>                                                                                       |
| \_XM \_ F16C \_ 內建函式\_      | DirectXMath 3.09 的新。 <br/> 當您指定這個編譯器指示詞時，DirectXMath 函式會實作為使用 SSE3、SSE 4.1、AVX 128 位和 F16C/CVT16 內建函式（如果適用）;否則 DirectXMath 會使用 SSE/SSE2。 當您使用 \_ xm \_ F16C \_ 內建函式時 \_ ，它會隱含的是 [xm AVX 內建] \_ 、[ \_ \_ \_ \_ xm SSE 內建函式] \_ 、[ \_ \_ \_ xm \_ SSE3 \_ \_ \_ \_ \_ \_ 內建] 和 [xm<br/>                                                                                                                                                 |
| \_XM \_ FMA3 \_ 內建函式\_      | DirectXMath 3.11 的新。 <br/> 當您指定這個編譯器指示詞時，DirectXMath 函式會在適用的情況下使用 SSE3、SSE 4.1、AVX 128 位和 FMA3 內建函式;否則 DirectXMath 會使用 SSE/SSE2。 當您使用 \_ xm \_ FMA3 \_ 內建函式時 \_ ，它會隱含的是 [xm AVX 內建] \_ 、[ \_ \_ \_ \_ xm SSE 內建函式] \_ 、[ \_ \_ \_ xm \_ SSE3 \_ \_ \_ \_ \_ \_ 內建] 和 [xm <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | 這可讓您使用 \_ \_ windows X86 或 windows x64 目標的 vectorcall 呼叫慣例。 \_ \_ \_ 當編譯器支援這項功能時，它會預設為 XM VECTORCALL = 1。 您可以手動將它設定為 \_ XM \_ VECTORCALL \_ = 0，以一律停用它。 <br/> \_\_Windows on ARM/ARM64 平臺或 Managed c + + 不支援 vectorcall。 <br/>                                                                                                                                                                                                                 |
| \_XM \_ SVML \_ 內建函式\_     | DirectXMath 3.16 的新。 <br/> 使用 VS 2019 或更新版本時，這可讓程式庫使用 &reg; 適用于 x86/x64 的 Intel Short 向量矩陣程式庫。 <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式設計參考](ovw-xnamath-reference.md)
</dt> </dl>

 

 
