---
description: 設定影片解碼所使用的背景工作執行緒數目。
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: 'CODECAPI_AVDecNumWorkerThreads 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973405"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>CODECAPI \_ AVDecNumWorkerThreads 屬性

設定影片解碼所使用的背景工作執行緒數目。

## <a name="data-type"></a>資料類型

**LONG** (**VT \_ I4**) 

## <a name="property-guid"></a>屬性 GUID

CODECAPI \_ AVDecNumWorkerThreads

## <a name="remarks"></a>備註

如果值為1，則此解碼器會選取執行緒的數目。

針對 [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) 介面，將此屬性設定為 **LONG** 值， (**VT \_ I4**) 。 針對 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面，將此屬性設定為 **UINT32**，雖然值已簽署。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

