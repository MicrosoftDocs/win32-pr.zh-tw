---
description: 釋放 IWiaPreview：： GetNewPreview 方法所快取的未篩選映射。 它也會釋放影像處理篩選。
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'IWiaPreview：： Clear 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972428"
---
# <a name="iwiapreviewclear-method"></a>IWiaPreview：： Clear 方法

釋放 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法所快取的未篩選映射。 它也會釋放影像處理篩選。

## <a name="syntax"></a>語法


```C++
void Clear();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

在 **IWiaPreview：： Clear** Windows 映像取得 (WIA) 2.0 Preview 元件會釋放它所儲存的所有介面指標。 WIA 2.0 Preview 元件會保留傳遞給 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)的 *pWiaItem2* 和 *pWiaTransferCallback* 參考。 為了精確起見，WIA 2.0 Preview 元件會保留 *pWiaItem2* 的參考和驅動程式的影像處理篩選，進而保留 *pWiaTransferCallback* 的參考。 在 **IWiaPreview：： Clear** 上，WIA 2.0 Preview 元件也會釋放其對 *pWiaItem2* 和影像處理篩選的參考，然後再釋放其對 *pWiaTransferCallback* 的參考。 WIA 2.0 Preview 元件會刪除其儲存在內部的快取、未篩選的影像。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




