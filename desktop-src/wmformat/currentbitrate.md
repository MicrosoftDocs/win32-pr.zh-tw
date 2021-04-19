---
title: CurrentBitrate
description: CurrentBitrate 屬性包含檔案中使用中資料流程目前的總位元速率。
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- CurrentBitrate windows Media 格式
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968878"
---
# <a name="currentbitrate"></a>CurrentBitrate

CurrentBitrate 屬性包含檔案中使用中資料流程目前的總位元速率。

## <a name="global-constant"></a>全域常數

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

這是程式碼屬性。

針對 **CurrentBitrate** 抓取的值會根據所使用的物件而有所不同。 在 [讀取器] 或 [同步讀取器] 物件中，值是呼叫時的實際位元速率。 在 [中繼資料編輯器] 物件中，值是檔案的平均位元速率。

檔案的實際位元速率等於所有使用中資料流程的位元速率，加上一些額外負荷。 例如，以 Windows Media Player 播放檔案時，就會顯示這個值。

這個屬性不能在檔案層級複製。 如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




