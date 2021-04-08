---
description: XAudio2 引擎的 debug 版本會驗證參數，並提供詳細的警告和錯誤訊息。
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: XAudio2 調試功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690883"
---
# <a name="xaudio2-debugging-facilities"></a>XAudio2 調試功能

XAudio2 引擎的 debug 版本會驗證參數，並提供詳細的警告和錯誤訊息。

## <a name="setting-the-debug-logging-level-at-run-time"></a>在執行時間設定 Debug 記錄層級

您可以使用所需的記錄層級的旗標填入 [**XAudio2 \_ DEBUG \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) 設定結構，然後將結構傳遞給 [**IXAudio2：： SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) 方法，隨時設定 XAudio2 所顯示的偵錯工具的層級。 傳遞給 **IXAudio2：： SetDebugConfiguration** 方法的值一律會覆寫在 Windows 登錄中設定的所有預設值。

## <a name="debug-support"></a>Debug 支援

在 Windows 8 中，偵錯工具一律可供 XAUDIO2。

針對 DirectX SDK 版本的 XAUDIO2，您必須在使用 [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)建立 XAUDIO2 物件時使用 **XAUDIO2 \_ DEBUG \_ ENGINE** ，而且系統必須安裝 DirectX SDK Developer Runtime，才能支援偵錯工具。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[調試功能](debugging-facilities.md)
</dt> <dt>

[XAudio2 程式設計參考](programming-reference.md)
</dt> </dl>

 

 
