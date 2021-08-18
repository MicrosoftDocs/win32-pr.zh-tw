---
title: WM/ContainerFormat
description: WM/ContainerFormat 屬性會指定在呼叫物件中載入的檔案類型。
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- WM/ContainerFormat windows Media 格式
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e0d5cc430b0580c6719d212d664d8c19ddc65eee64e5877a8e6aba80d94a6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839438"
---
# <a name="wmcontainerformat"></a>WM/ContainerFormat

**WM/ContainerFormat** 屬性會指定在呼叫物件中載入的檔案類型。

## <a name="global-constant"></a>全域常數

g \_ wszWMContainerFormat

## <a name="data-type"></a>資料類型

[**WMT \_ (\_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) **WMT \_ 類型 \_ 二進位**) 的儲存格式

## <a name="remarks"></a>備註

這個屬性是用來取代不再支援的 **IWMProfile3：： GetStorageFormat** 和 **IWMProfile3：： SetStorageFormat**。

這是程式碼屬性。

這個屬性不能在檔案層級複製。 如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其正常意義傳遞給 Windows 媒體格式 SDK 的物件。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




