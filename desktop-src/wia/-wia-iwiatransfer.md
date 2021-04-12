---
description: IWiaTransfer 介面會提供資料流程傳輸的資料。
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: 'IWiaTransfer 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191395"
---
# <a name="iwiatransfer-interface"></a>IWiaTransfer 介面

**IWiaTransfer** 介面會提供資料流程傳輸的資料。

## <a name="members"></a>成員

**IWiaTransfer** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IWiaTransfer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWiaTransfer** 介面具有這些方法。



| 方法                                                                 | 描述                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**取消**](-wia-iwiatransfer-cancel.md)                             | 取消目前的傳送作業。 <br/>                                         |
| [**下載**](-wia-iwiatransfer-download.md)                         | 起始將資料下載至呼叫端。 <br/>                                        |
| [**EnumWIA \_ 格式 \_ 資訊**](-wia-iwiatransfer-enumwia-format-info.md) | 針對 WIA 2.0 裝置支援的傳輸格式建立枚舉器。<br/> |
| [**上傳**](-wia-iwiatransfer-upload.md)                             | 從呼叫端起始單一專案的資料上傳。 <br/>                       |



 

## <a name="remarks"></a>備註

**IWiaTransfer** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。



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



 

 
