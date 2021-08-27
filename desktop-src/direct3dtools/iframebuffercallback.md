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
ms.openlocfilehash: 479796ebf225ceac4e93f429aa6b8412e3f86398
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628836"
---
# <a name="span-idvspixengineiframebuffercallbackspaniframebuffercallback-interface"></a><span id="vspixengine.iframebuffercallback"></span>IFrameBufferCallback 介面

回呼，以傳回轉譯目標。 不論引擎內 rendertarget 的格式為何，傳回轉譯目標的格式都是 R8G8B8A8 \_ UNORM。

## <a name="members"></a>成員

**IFrameBufferCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IFrameBufferCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>方法

**IFrameBufferCallback** 介面具有這些方法。

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th style="text-align: left;">方法</th><th style="text-align: left;">描述</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/iframebuffercallback-resultcallback-dword-dword-dword-dword-double-dword-byte-arr"><strong>ResultCallback</strong></a></td><td style="text-align: left;"><p>回呼，會通知主機相關要求所傳回的畫面格緩衝區資訊。</p></td></tr></tbody></table>

 

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 
