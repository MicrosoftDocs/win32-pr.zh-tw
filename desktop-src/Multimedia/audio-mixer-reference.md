---
title: 音訊 Mixer 參考
description: 音訊 Mixer 參考
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- 多媒體音訊、音訊 mixers
- 音訊、音訊 mixers
- 多媒體音訊、混音器參考
- 音訊、混音器參考
- 音訊 mixers，參考
- mixers，參考
- 音訊 mixers 的參考，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1602a9ac0631a3e81430285c8cd862215a437c72b03b41d87fad6cefa7e41827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786218"
---
# <a name="audio-mixer-reference"></a>音訊 Mixer 參考

本節說明與音訊 mixers 相關聯的函式、結構和訊息。 這些元素的分組方式如下。

## <a name="querying-devices"></a>查詢裝置

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>開啟和關閉

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>正在抓取 Mixer 識別碼

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>正在抓取線條控制項

-   [**MIXERCONTROL**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>變更控制項屬性

-   [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS \_ 布林值**](/previous-versions//dd757295(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ 簽署**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ 未簽署**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>正在抓取行資訊

-   [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**MM \_ MIXM \_ 控制項 \_ 變更**](mm-mixm-control-change.md)
-   [**MM \_ MIXM \_ 行 \_ 變更**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>傳送 User-Defined 訊息

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊 Mixer 參考](audio-mixer-reference.md)
</dt> </dl>

 

 