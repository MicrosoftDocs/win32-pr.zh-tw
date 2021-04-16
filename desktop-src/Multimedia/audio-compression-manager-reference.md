---
title: 音訊壓縮管理員參考
description: 音訊壓縮管理員參考
ms.assetid: a4e234c7-4dd3-4269-90a5-5de2c8837c0f
keywords:
- Windows 多媒體、進行中的參考
- 多媒體、進行中的參考
- 多媒體音訊、進行中的參考
- '音訊、進行中的參考) '
- 音訊壓縮管理員 (的) ，參考
- " (音效壓縮管理員) ，參考"
- 資訊相關參考，關於
- 對等
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d365b0a69ecd94a07811b24762aa4bffdc8c9f1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507871"
---
# <a name="audio-compression-manager-reference"></a>音訊壓縮管理員參考

本章節描述與此架構相關聯的函式、結構和訊息。 這些元素的分組方式如下。

## <a name="drivers"></a>驅動程式

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverClose**](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [**ACMDRIVERDETAILS**](/windows/win32/api/msacm/ns-msacm-acmdriverdetails)
-   [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmDriverID**](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [**acmDriverMessage**](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [**acmDriverOpen**](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

## <a name="filters"></a>篩選器

-   [**ACMFILTERCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmfilterchoose)
-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**ACMFILTERDETAILS**](/windows/win32/api/msacm/ns-msacm-acmfilterdetails)
-   [**acmFilterEnum**](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**ACMFILTERTAGDETAILS**](/windows/win32/api/msacm/ns-msacm-acmfiltertagdetails)
-   [**acmFilterTagEnum**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)

## <a name="formats"></a>格式

-   [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [**ACMFORMATDETAILS**](/windows/win32/api/msacm/ns-msacm-acmformatdetails)
-   [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [**ACMFORMATTAGDETAILS**](/windows/win32/api/msacm/ns-msacm-acmformattagdetails)
-   [**acmFormatTagEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)

## <a name="messages"></a>訊息

-   [**MM \_ \_ FILTERCHOOSE**](mm-acm-filterchoose.md)
-   [**MM \_ \_ FORMATCHOOSE**](mm-acm-formatchoose.md)

## <a name="streams"></a>串流

-   [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))
-   [**ACMSTREAMHEADER**](/windows/win32/api/msacm/ns-msacm-acmstreamheader)
-   [**acmStreamMessage**](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [**acmStreamReset**](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="miscellaneous"></a>其他

-   [**acmGetVersion**](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊壓縮管理員](audio-compression-manager.md)
</dt> </dl>

 

 