---
title: HasAttachedImages
description: HasAttachedImages 屬性是檔案層級屬性，用來指定檔案是否為具有附加之 APIC ID3 框架的 MP3 檔案。
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- HasAttachedImages windows Media 格式
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106999584"
---
# <a name="hasattachedimages"></a>HasAttachedImages

**HasAttachedImages** 屬性是檔案層級屬性，用來指定檔案是否為具有附加之 APIC ID3 框架的 MP3 檔案。

## <a name="global-constant"></a>全域常數

g \_ wszWMHasAttachedImages

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ BOOL**

## <a name="remarks"></a>備註

這是程式碼屬性。

這個屬性不能在檔案層級複製。 如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。

**HasAttachedImages** 的設計目的是要通知應用程式有映射存在，以便使用 [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) 介面來抓取影像。 現在已使用 [**WM/Picture**](wmpicture.md) 屬性支援映射，因此不再需要 **HasAttachedImages** 。

若要判斷檔案是否包含影像，請呼叫 [**IWMHeaderInfo3：： GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) 來指定 **WM/圖片** 屬性。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




