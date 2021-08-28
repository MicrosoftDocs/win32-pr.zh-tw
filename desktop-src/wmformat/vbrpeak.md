---
title: VBRPeak
description: VBRPeak 屬性包含變數位元速率的最高暫時位速率 (VBR) 編碼的資料流程。
ms.assetid: 7b735145-8235-4efb-986f-952989b739bc
keywords:
- VBRPeak windows Media 格式
topic_type:
- apiref
api_name:
- VBRPeak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9163e64aa3d309af8fd35626b7a4c0397ba4c949213ef351c1ac73ee9575a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704838"
---
# <a name="vbrpeak"></a>VBRPeak

**VBRPeak** 屬性包含變數位元速率的最高暫時位速率 (VBR) 編碼的資料流程。

## <a name="global-constant"></a>全域常數

g \_ wszVBRPeak

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

存取寫入器物件的 **IWMHeaderInfo3** 介面時，您可以加入或變更此值。 在其他物件 (中繼資料編輯器、讀取器和同步讀取器) ，此值是唯讀的。

寫入器會自動為每個 VBR 串流寫入 **VBRPeak** 值。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




