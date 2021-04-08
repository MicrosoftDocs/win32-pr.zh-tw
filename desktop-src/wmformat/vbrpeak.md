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
ms.openlocfilehash: 6e8aacb076c3e92cfa676e73e945506cc4942bf4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022566"
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

 

 




