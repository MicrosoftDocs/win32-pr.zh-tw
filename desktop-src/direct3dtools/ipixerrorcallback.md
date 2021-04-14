---
description: 從引擎回呼以處理錯誤。
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPixErrorCallback 介面
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385630"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback 介面

從引擎回呼以處理錯誤。

## <a name="members"></a>成員

**IPixErrorCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IPixErrorCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="span-idmethodsspanmethods"></a><span id="methods"></span>方法

**IPixErrorCallback** 介面具有這些方法。

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;">方法</th><th style="text-align: left;">描述</th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></td><td style="text-align: left;"><p>回呼，會通知主機相關要求所傳回的錯誤。</p></td></tr><tr class="even"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></td><td style="text-align: left;"><p>回呼，會通知主機相關要求所傳回的訊息。</p></td></tr><tr class="odd"><td style="text-align: left;"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></td><td style="text-align: left;"><p>回呼，會通知主機相關要求所傳回的警告。</p></td></tr></tbody></table>

 

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 
