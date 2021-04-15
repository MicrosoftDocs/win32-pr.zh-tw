---
description: 用於傳達 vsglog 相關資料的原始介面。
MS-HAID: vspixengine.IPixEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixEngine 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87AB1D07-8E90-49F0-B44D-F6185923B8D4
api_name:
- IPixEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2f02538f7acbd88daf166af657382e507a4e5661
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467922"
---
# <a name="span-idvspixengineipixenginespanipixengine-interface"></a><span id="vspixengine.ipixengine"></span>IPixEngine 介面

用於傳達 vsglog 相關資料的原始介面。

## <a name="members"></a>成員

**IPixEngine** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPixEngine** 也有下列類型的成員：

-   [方法](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>方法

**IPixEngine** 介面具有這些方法。

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">方法</th><th style="text-align: left;">描述</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-openfile-bstr-bstr-inewframescallback-ptr-ifileiocallback-ptr-lcid"><strong>OpenFile</strong></a></td><td style="text-align: left;"><p>開啟圖形記錄檔。</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-runexperiment-experiment-irunexperimentcallback-ptr-inewframescallback-ptr-ifileiocallback-ptr-dword-experimenttrigger-arr"><strong>RunExperiment</strong></a></td><td style="text-align: left;"><p>執行實驗。</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-savefile-bstr-ifileiocallback-ptr"><strong>SaveFile</strong></a></td><td style="text-align: left;"><p>將圖形記錄檔儲存至指定的位置。</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-setparentprocess-dword"><strong>SetParentProcess</strong></a></td><td style="text-align: left;"><p>未使用。</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixengine-shutdown"><strong>關閉</strong></a></td><td style="text-align: left;"><p>關閉引擎。</p></td></tr></tbody></table>

 

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 
