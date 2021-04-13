---
description: IWiaTransferCallback 介面會在資料傳輸期間接收回呼。
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: 'IWiaTransferCallback 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113293"
---
# <a name="iwiatransfercallback-interface"></a>IWiaTransferCallback 介面

**IWiaTransferCallback** 介面會在資料傳輸期間接收回呼。

## <a name="members"></a>成員

**IWiaTransferCallback** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaTransferCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaTransferCallback** 介面具有這些方法。



| 方法                                                                 | 描述                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md)       | 取得指定之專案的新資料流程。 <br/>                    |
| [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) | 提供傳輸期間的進度和其他通知。 <br/> |



 

## <a name="remarks"></a>備註

影像處理篩選器開發人員應該執行這個介面和 [**IWiaImageFilter**](-wia-iwiaimagefilter.md) 介面。

**IWiaTransferCallback** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。



| IUnknown 方法                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | 傳回受支援介面的指標。 |
| [IUnknown：： AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | 遞增參考次數。               |
| [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | 遞減參考次數。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl>     |
| 程式庫<br/>                  | <dl> <dt>Wiaguid .lib</dt> </dl> |



 

 
