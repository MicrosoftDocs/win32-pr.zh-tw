---
description: 表示來自 >mediastreamsource 的範例要求。
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: IMFMediaStreamSourceSampleRequest 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321580"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a>IMFMediaStreamSourceSampleRequest 介面

表示來自 >mediastreamsource 的範例要求。

## <a name="members"></a>成員

**IMFMediaStreamSourceSampleRequest** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IMFMediaStreamSourceSampleRequest** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IMFMediaStreamSourceSampleRequest** 介面具有這些方法。



| 方法                                                           | 描述                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**SetSample**](imfmediastreamsourcesamplerequest-setsample.md) | 設定媒體資料流程來源的範例。<br/> |



 

## <a name="remarks"></a>備註

**MFMediaStreamSourceSampleRequest** 是由 [**MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) 執行時間類別所執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                       |
| Idl<br/>                      | <dl> <dt>Mfidl .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎介面](media-foundation-interfaces.md)
</dt> </dl>

 

 
