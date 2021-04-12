---
title: 儲存64位值
description: 若要儲存64位指標值，請使用 ULONG \_ PTR。 當使用 \_ 32 位編譯器編譯時，ULONG PTR 值為32位，而當以64位編譯器編譯時，則為64位。
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- 儲存64位值64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cee4826caf93dbd464957fb5fb76f024bd9f41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300895"
---
# <a name="storing-a-64-bit-value"></a>儲存64位值

若要儲存64位指標值，請使用 **ULONG \_ PTR**。 當使用32位編譯器編譯時， **ULONG \_ PTR** 值為32位，而當以64位編譯器編譯時，則為64位。

下列範例會使用已移植到64位 Windows 的真實世界程式碼。 包含將程式碼與64位相容的步驟的評論。

## <a name="example-1-getting-an-address"></a>範例1：取得位址

下列程式碼說明可攜取得位址的方式。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>使用 ULONG (僅限32位的方法) </td>
<td><pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )
Int *somePointer
Return( (ULONG) somePointer );</code></pre></td>
</tr>
<tr class="even">
<td>使用 ULONG_PTR (可移植方法) </td>
<td><pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )
Int *somePointer
Return( (ULONG_PTR) somePointer );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="example-2-calculating-an-address"></a>範例2：計算位址

下列程式碼說明可移植的方式來計算位址。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>使用 ULONG (僅限32位的方法) </td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre></td>
</tr>
<tr class="even">
<td>使用 ULONG_PTR (可移植方法) </td>
<td><pre class="syntax" data-space="preserve"><code>Int *somePointer;
Int *someOtherPointer;
somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre></td>
</tr>
</tbody>
</table>



 

 

 




