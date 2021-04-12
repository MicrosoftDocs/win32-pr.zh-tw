---
description: 設定影片編碼器所使用的背景工作執行緒數目。
ms.assetid: E490DF0C-97DE-4375-A4DB-17DA4E782E2D
title: 'CODECAPI_AVEncNumWorkerThreads 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e08e18f57478597b841e042b17c601451ad93cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191080"
---
# <a name="codecapi_avencnumworkerthreads-property"></a>CODECAPI \_ AVEncNumWorkerThreads 屬性

設定影片編碼器所使用的背景工作執行緒數目。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncNumWorkerThreads**

## <a name="remarks"></a>備註

如果值為零，則編碼器會選取執行緒的數目。

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

 

