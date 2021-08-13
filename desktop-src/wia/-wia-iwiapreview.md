---
description: IWiaPreview 介面會在內部快取未篩選的影像，並透過影像處理篩選器來傳遞它們。
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: 'IWiaPreview 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e2672211e5c1a17fa360a6078069ae8260687dc896843ffb6bf572d9b7be8caa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442068"
---
# <a name="iwiapreview-interface"></a>IWiaPreview 介面

**IWiaPreview** 介面會在內部快取未篩選的影像，並透過影像處理篩選器來傳遞它們。

## <a name="members"></a>成員

**IWiaPreview** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaPreview** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaPreview** 介面具有這些方法。



| 方法                                                  | 描述                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**清除**](-wia-iwiapreview-clear.md)                 | 釋放 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法所快取的未篩選映射。 它也會釋放影像處理篩選。 <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | 叫用驅動程式分割篩選，並將 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法快取的未篩選影像傳遞至篩選。 <br/> |
| [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) | 在內部快取從驅動程式傳回之未篩選的映射。 <br/>                                                                                                                |
| [**UpdatePreview**](-wia-iwiapreview-updatepreview.md) | 取得 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法快取的未篩選影像。 <br/>                                                            |



 

## <a name="remarks"></a>備註

[**IWiaTransfer：:D 下載 o)**](-wia-iwiatransfer-download.md)方法會自動呼叫此篩選器。

**IWiaPreview** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。



| IUnknown 方法                                        | 描述                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | 傳回受支援介面的指標。 |
| [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | 遞增參考次數。               |
| [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | 遞減參考次數。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
