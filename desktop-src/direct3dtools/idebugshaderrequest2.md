---
description: 開始對著色器進行調試的要求。 此要求包含兩個部分：產生追蹤，以及對追蹤進行 debug 錯。
MS-HAID: vspixengine.IDebugShaderRequest2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 80F95900-F2E6-4B5C-B902-573280956E94
api_name:
- IDebugShaderRequest2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9b508cd8f8e4dfb98f3a4cfd758599affb2bdfaf05fb97afe9fbeac8e18e4b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283737"
---
# <a name="span-idvspixengineidebugshaderrequest2spanidebugshaderrequest2-interface"></a><span id="vspixengine.idebugshaderrequest2"></span>IDebugShaderRequest2 介面

開始對著色器進行調試的要求。 此要求包含兩個部分：產生追蹤，以及對追蹤進行 debug 錯。

## <a name="members"></a>成員

**IDebugShaderRequest2** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IDebugShaderRequest2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>方法

**IDebugShaderRequest2** 介面具有這些方法。

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">方法</th><th style="text-align: left;">描述</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-begindebugshader-ipixerrorcallback-ptr-dword-byte-arr-dword-ptr"><strong>BeginDebugShader</strong></a></td><td style="text-align: left;"><p>要求開始對指定的資訊清單進行偵錯工具。</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/idebugshaderrequest2-generateinstructions-ipixerrorcallback-ptr-debugshaderrequestinfo-ptr-pixelhistoryoperation-ptr-idebugshadercallback-ptr"><strong>GenerateInstructions</strong></a></td><td style="text-align: left;"><p>在 debug 要求中產生著色器追蹤指令的要求。 以追蹤為基礎的偵錯工具會發生在 CPU (變形) ，而不是 GPU。</p></td></tr></tbody></table>

 

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 
