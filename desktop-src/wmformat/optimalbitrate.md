---
title: OptimalBitrate
description: OptimalBitrate 屬性包含最佳播放檔案的位元速率。
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- OptimalBitrate windows Media 格式
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968469"
---
# <a name="optimalbitrate"></a>OptimalBitrate

**OptimalBitrate** 屬性包含最佳播放檔案的位元速率。

## <a name="global-constant"></a>全域常數

g \_ wszWMOptimalBitrate

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ DWORD**

## <a name="remarks"></a>備註

這是程式碼屬性。

針對包含變數位元速率 (VBR) 資料流程的檔案，這個值是檔案中資料流程的尖峰位元速率。 針對沒有 VBR 的檔案，此值與 [**位元速率**](bit-rate.md)相同。

這個屬性不能在檔案層級複製。 如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




