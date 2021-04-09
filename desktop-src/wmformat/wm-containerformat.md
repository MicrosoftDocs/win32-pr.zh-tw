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
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678595"
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

這個屬性不能在檔案層級複製。 如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性清單**](attribute-list.md)
</dt> </dl>

 

 




