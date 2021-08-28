---
description: 回呼，以傳回轉譯目標。 不論引擎內 rendertarget 的格式為何，傳回轉譯目標的格式都是 R8G8B8A8 \_ UNORM。
MS-HAID: vspixengine.IFrameBufferCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IFrameBufferCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 613AD7AC-0732-49E2-8155-AE0A76597BE9
api_name:
- IFrameBufferCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7705f055fe09839d1e4afe22a9d779ca859ec3ba
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786534"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback 介面

回呼，以傳回轉譯目標。 不論引擎內 rendertarget 的格式為何，傳回轉譯目標的格式都是 R8G8B8A8 \_ UNORM。

## <a name="members"></a>成員

**IFrameBufferCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IFrameBufferCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>方法

**IFrameBufferCallback** 介面具有這些方法。

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >方法</th><th >說明</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></td><td ><p>回呼，會通知主機相關要求所傳回的畫面格緩衝區資訊。</p></td></tr></tbody></table>

 

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 
