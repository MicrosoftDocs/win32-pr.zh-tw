---
description: 從引擎回呼，表示它已完成剖析新增至記錄檔的任何新框架。
MS-HAID: vspixengine.INewFramesCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: INewFramesCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A73E1EA4-F9D5-43F1-B363-20B3F7B3D8B0
api_name:
- INewFramesCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8b5e27183461ca1eb0e214000551e18c08d2914f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631416"
---
# <a name="span-idvspixengineinewframescallbackspaninewframescallback-interface"></a><span id="vspixengine.inewframescallback"></span>INewFramesCallback 介面

從引擎回呼，表示它已完成剖析新增至記錄檔的任何新框架。

## <a name="members"></a>成員

**INewFramesCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INewFramesCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>方法

**INewFramesCallback** 介面具有這些方法。

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">方法</th><th style="text-align: left;">描述</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelall"><strong>CancelAll</strong></a></td><td style="text-align: left;"><p>通知主機所有要求都已取消的回呼。</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcallback-iunknown-ptr"><strong>CancelUsingCallback</strong></a></td><td style="text-align: left;"><p>通知主機已取消要求的回呼。</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-cancelusingcookie-dword"><strong>CancelUsingCookie</strong></a></td><td style="text-align: left;"><p>回呼，使用可唯一識別要求的 cookie 來通知主機已取消的要求。</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/inewframescallback-newframesavailable"><strong>NewFramesAvailable</strong></a></td><td style="text-align: left;"><p>回呼，會通知主機有新的框架可供處理。</p></td></tr></tbody></table>

 

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 
