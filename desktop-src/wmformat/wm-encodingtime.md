---
title: WM/EncodingTime
description: WM/EncodingTime 屬性包含內容編碼時間的時間戳記。
ms.assetid: 63da9392-264d-40bb-99fd-56db93801941
keywords:
- WM/EncodingTime windows Media 格式
topic_type:
- apiref
api_name:
- WM/EncodingTime
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d27119a9b54e3de22fe620f556c672bd4fe1a17
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022663"
---
# <a name="wmencodingtime"></a>WM/EncodingTime

**WM/EncodingTime** 屬性包含內容編碼時間的時間戳記。

## <a name="global-constant"></a>全域常數

g \_ wszWMEncodingTime

## <a name="data-type"></a>資料類型

**FILETIME** (**WMT \_ 類型 \_ QWORD**) 

## <a name="remarks"></a>備註

這個屬性會使用 FILETIME 值，這是代表自1601年1月1日以來經過的 100-納秒時間單位數的64位值。 如需 FILETIME 的詳細資訊，請參閱 Platform SDK 的 Windows 系統資訊一節。

這不是編碼屬性。 如果您想要將它包含在您的檔案中，則必須手動設定它。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




