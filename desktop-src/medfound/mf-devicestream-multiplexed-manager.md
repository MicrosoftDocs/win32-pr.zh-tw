---
description: 提供 IMFMuxStreamAttributesManager 的實例，此實例會管理描述多工媒體來源子串流的 IMFAttributes。
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: 'MF_DEVICESTREAM_MULTIPLEXED_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975001"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a>MF \_ DEVICESTREAM 多工 \_ \_ 管理器屬性

提供 [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) 的實例，此實例會管理描述多工媒體來源子串流的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 。

## <a name="data-type"></a>資料類型

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>備註

將此值傳遞至 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) ，以判斷媒體來源是否提供多工資料流程，如果是，則取得 [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager)的實例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



 

 
