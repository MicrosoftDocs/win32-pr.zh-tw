---
description: 用來查看材質的回呼。
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine5Callbacks 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 75124025c2857f98f71934b1e3848b3b7ac186ac
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786304"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks 介面

用來查看材質的回呼。

## <a name="members"></a>成員

**IPixEngine5Callbacks** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPixEngine5Callbacks** 也有下列類型的成員：

-   [方法](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>方法

**IPixEngine5Callbacks** 介面具有這些方法。

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th >方法</th><th >說明</th></tr></thead><tbody><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></td><td ><p>釋放材質時，用來通知主機的回呼函式。</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></td><td ><p>當長條圖載入已完成時，用來通知主機的回呼函式。</p></td></tr><tr class="odd"><td ><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></td><td ><p>當材質載入已完成時，用來通知主機的回呼函式。</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></td><td ><p>當材質配量載入已完成時，用來通知主機的回呼函式。</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></td><td ><p>當材質值讀取完成時，用來通知主機的回呼函數。</p></td></tr><tr class="even"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></td><td ><p>在紋理轉譯完成時，用來通知主機的回呼函式。</p></td></tr><tr class="odd"><td ><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></td><td ><p>在儲存材質時，用來通知主控制項的回呼函式已完成。</p></td></tr></tbody></table>

 

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 
