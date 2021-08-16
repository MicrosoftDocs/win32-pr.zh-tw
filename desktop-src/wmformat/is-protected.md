---
title: Is_Protected
description: '\_受保護的屬性是檔案層級屬性，用來指定是否使用數位版權管理 (DRM) 保護檔案中的內容。'
ms.assetid: 6fe63d9b-67ec-47a8-ba20-657434c7a15b
keywords:
- Is_Protected windows Media 格式
topic_type:
- apiref
api_name:
- Is_Protected
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0759dfc781409a1331403c3b02c2645f6ad843925584eab2a55f31a0c8d31af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847415"
---
# <a name="is_protected"></a>\_受保護

**\_ 受保護** 的屬性是檔案層級屬性，用來指定是否使用數位版權管理 (DRM) 保護檔案中的內容。

## <a name="global-constant"></a>全域常數

g \_ wszWMProtected

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

這是程式碼屬性。 抓取此屬性會提供與呼叫 [**WMIsContentProtected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmiscontentprotected)相同的資訊。

這個屬性不能在檔案層級複製。 如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其正常意義傳遞給 Windows 媒體格式 SDK 的物件。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




