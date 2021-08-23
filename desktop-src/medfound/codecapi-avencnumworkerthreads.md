---
description: 設定影片編碼器所使用的背景工作執行緒數目。
ms.assetid: E490DF0C-97DE-4375-A4DB-17DA4E782E2D
title: 'CODECAPI_AVEncNumWorkerThreads 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fe4a025ce47e7c9775b677c3ef5a72d55f892ae201f5241421a2ff0d29163
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974907"
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
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

