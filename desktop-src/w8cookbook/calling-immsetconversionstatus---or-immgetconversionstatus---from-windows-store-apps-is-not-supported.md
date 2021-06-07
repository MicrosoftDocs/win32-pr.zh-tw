---
title: '不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () '
description: '不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () '
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443142"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a>不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () 

## <a name="platforms"></a>平台

<dl> 用戶端-windows 8。1  
伺服器-Windows Server 2012 R2  
</dl>

## <a name="description"></a>描述

不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () ，而且可能會導致非預期的結果。

## <a name="manifestations"></a>表現

在應用程式啟動時，IME 模式會設定為下列預設值：



| &nbsp;   | 軟體輸入面板 | 硬體鍵盤 |
|----------|----------------------|-------------------|
| KOR、JPN | 開啟                   | 關閉               |
| CHS、CHT | 開啟                   | 開啟                |



 

## <a name="solution"></a>解決方法

開發人員可以藉由指定欄位的輸入範圍值，來控制預設的 IME 模式。

指定輸入範圍的輸入法模式取決於每個 IME。 開發人員無法指定 IME 模式。

## <a name="resources"></a>資源

-   [InputScope 列舉](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [ImmSetConversionStatus](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   [ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))

 

 