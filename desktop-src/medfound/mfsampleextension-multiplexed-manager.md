---
description: 提供用來從多工媒體來源的子串流存取樣本集合的 IMFMuxStreamSampleManager 實例。
ms.assetid: 4FD8169D-FDDF-4C69-AD46-05B02B35028C
title: 'MFSampleExtension_MULTIPLEXED_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b46c277265538ccb2b990ea9d912b9337bcd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979075"
---
# <a name="mfsampleextension_multiplexed_manager-attribute"></a>MFSampleExtension 多工 \_ \_ 管理器屬性

提供用來從多工媒體來源的子串流存取樣本集合的 [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager) 實例。

## <a name="data-type"></a>資料類型

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>備註

將此值傳遞至 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) ，以取得 [**IMFMuxStreamSampleManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager)的實例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



 

 
