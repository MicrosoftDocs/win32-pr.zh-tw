---
title: Is_Trusted
description: 是 \_ 受信任的屬性是檔案層級屬性，可指定檔案中的授權取得 URL 是否受信任。
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted windows Media 格式
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e255c91c5779eb44da8e587601fdfd9264f10888a46a7f216ae2af619ff9f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198274"
---
# <a name="is_trusted"></a>\_受信任

**是 \_ 受信任** 的屬性是檔案層級屬性，可指定檔案中的授權取得 URL 是否受信任。

## <a name="global-constant"></a>全域常數

g \_ wszWMTrusted

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

這是程式碼屬性。

在流覽至包含在受 DRM 保護之檔案中的授權取得 URL 之前，應用程式應該先確認此屬性為 true。 如果為 false，則應用程式應該通知使用者 URL 可能已遭篡改。

這個屬性不能在檔案層級複製。 如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其正常意義傳遞給 Windows 媒體格式 SDK 的物件。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




