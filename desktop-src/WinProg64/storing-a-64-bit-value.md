---
title: 儲存64位值
description: 若要儲存64位指標值，請使用 ULONG \_ PTR。 當使用 \_ 32 位編譯器編譯時，ULONG PTR 值為32位，而當以64位編譯器編譯時，則為64位。
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- Windows 程式設計儲存64位值64位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b23de4fc4c15205e142a7a468d5a1bc5247ee9be23f0ca1bea1a0c28284d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113493"
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



 

 

 




