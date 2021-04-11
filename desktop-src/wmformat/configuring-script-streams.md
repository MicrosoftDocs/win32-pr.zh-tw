---
title: 設定腳本資料流程
description: 設定腳本資料流程
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- 資料流程，設定腳本資料流程
- 編解碼器，設定腳本資料流程
- 編寫資料流程的腳本，設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021321"
---
# <a name="configuring-script-streams"></a>設定腳本資料流程

就像所有的任意資料流程類型一樣，腳本資料流程必須為它們定義位元速率和緩衝區視窗。 在 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構中的主要媒體類型必須設定為 WMMEDIATYPE \_ 腳本。

腳本資料流程必須將 **WM \_ 媒體 \_ 類型** 的 **formattype** 成員設定為 WMFORMAT \_ 腳本，這表示 **pbFormat** 成員指向 [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)結構。

只有一個支援的腳本類型： WMSCRIPTTYPE \_ TwoStrings。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定任意資料流程類型**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**指令碼命令**](script-commands.md)
</dt> </dl>

 

 




