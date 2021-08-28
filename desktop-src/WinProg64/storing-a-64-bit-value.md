---
title: 儲存64位值
description: 若要儲存64位指標值，請使用 ULONG \_ PTR。 當使用 \_ 32 位編譯器編譯時，ULONG PTR 值為32位，而當以64位編譯器編譯時，則為64位。
ms.assetid: 0712e084-cf5e-470a-8f5d-0db2ef638f42
keywords:
- Windows 程式設計儲存64位值64位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6be70aba73af9640a69aa60055afcfb03ade7a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469065"
---
# <a name="storing-a-64-bit-value"></a>儲存64位值

若要儲存64位指標值，請使用 **ULONG \_ PTR**。 當使用32位編譯器編譯時， **ULONG \_ PTR** 值為32位，而當以64位編譯器編譯時，則為64位。

下列範例會使用已移植到64位 Windows 的真實世界程式碼。 包含將程式碼與64位相容的步驟的評論。

## <a name="example-1-getting-an-address"></a>範例1：取得位址

下列程式碼說明可攜取得位址的方式。




| | |使用 ULONG (僅限32位的方法) | <pre class="syntax" data-space="preserve"><code>ULONG getAnAddress( )Int *somePointerReturn( (ULONG) somePointer );</code></pre> | |使用 ULONG_PTR (可移植方法) | <pre class="syntax" data-space="preserve"><code>ULONG_PTR getAnAddress( )Int *somePointerReturn( (ULONG_PTR) somePointer );</code></pre> | 




 

## <a name="example-2-calculating-an-address"></a>範例2：計算位址

下列程式碼說明可移植的方式來計算位址。




| | |使用 ULONG (僅限32位的方法) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG)someOtherPointer + 0x20 );</code></pre> | |使用 ULONG_PTR (可移植方法) | <pre class="syntax" data-space="preserve"><code>Int *somePointer;Int *someOtherPointer;somePointer = (int *)( (ULONG_PTR)someOtherPointer + 0x20 );</code></pre> | 




 

 

 




