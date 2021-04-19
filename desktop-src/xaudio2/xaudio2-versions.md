---
description: XAudio2 是一種跨平臺 API，隨附于 Xbox 360 及 Windows 版本，包括 Windows XP、Windows Vista、Windows 7 和 Windows 8。
ms.assetid: 875b44c4-30d6-8a6e-0cfc-9beb8c46f1b4
title: XAudio2 版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c9facfe357c323bd8f7b607460a8f59bd062fe
ms.sourcegitcommit: 010f524cd6098a5941de77907d4d6ae7871f8af1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "106982127"
---
# <a name="xaudio2-versions"></a>XAudio2 版本

XAudio2 是一種跨平臺 API，隨附于 Xbox 360 及 Windows 版本，包括 Windows XP、Windows Vista、Windows 7 和 Windows 8。 在 Xbox 360 上，XAudio2 會以靜態程式庫的形式提供，並編譯成主要的遊戲可執行檔。 在 Windows 中，XAudio2 是以動態連結程式庫的形式提供， (DLL) 安裝到作業系統的系統資料夾中。

## <a name="xaudio-29-windows-10-and-redistributable-for-windows-7-and-windows-8x"></a>適用于 Windows 7 和 Windows 8 x 的 XAudio 2.9 (Windows 10 和可轉散發套件) 

XAudio2 2.9 版隨附于 Windows 10、XAUDIO2 \_9.DLL，以及 XAudio 2.8 以支援較舊的應用程式。 [XAudio 2.9](xaudio2-redistributable.md)的可轉散發版本也適用于 WINDOWS 7 SP1、Windows 8 和 Windows 8.1。

XAudio 2.9 已更新下列變更：

-   新建立旗標： XAUDIO2 \_ DEBUG \_ ENGINE、XAUDIO2 \_ STOP \_ ENGINE \_ WHEN \_ IDLE、XAUDIO2 \_ 1024 \_ 量子
-   此版本的 XAudio2 提供 xWMA 支援。
-   Windows 10 版本的 XAudio 2.9 支援 [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) 函數。
-   [**XAUDIO2FX \_立即的 \_ 參數**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) 現在包含7.1 系統的值 *SideDelay* 。
-   [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)函式現在包含啟用7.1 回音的布林 *sevenDotOneReverb* 參數。

## <a name="xaudio-28-windows-8x"></a>XAudio 2.8 (Windows 8 x) 

XAudio2 2.8 版現在隨附于 Windows 8，XAUDIO28.DLL 的系統元件 \_ 。 這是可用的「收件匣」，不需要與應用程式一起轉散發。 建議您使用 Windows 軟體開發套件 (SDK) 進行 Windows 8，以針對 XAudio2 進行開發;Windows 8 的 Windows SDK 包含必要的標頭和匯入程式庫，以針對 XAUDIO28.DLL 進行靜態連結 \_ 。

XAudio2 2.8 已更新下列變更：

-   此版本支援 Windows Store 應用程式開發;XAudio2 API 可以在 c + +/DirectX Windows Store 應用程式中使用。
-   [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) 是一般的 WIN32 API 呼叫，不再建立 XAudio2 CLSID。 已移除由 CoCreateInstance 將 XAudio2 具現化的支援。
-   初始化函式現在已由建立程式隱含呼叫，且已從 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 介面中移除。
-   裝置列舉功能已從 XAudio2 中移除;GetDeviceDetails 和 GetDeviceCount 函數已從 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 介面中移除。 想要轉譯至系統上其他音訊裝置的應用程式，必須將裝置識別碼字串傳遞至 [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) ，而不是裝置索引。 仍可建立預設音訊轉譯裝置，但不含列舉。
-   [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) 具有新增的函式 [**IXAudio2MasteringVoice：： GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) ，會傳回目的地輸出裝置的通道遮罩。
-   [X3DAudio](x3daudio.md)和[XAPOFX](xapofx-overview.md)程式庫會合並到 XAudio2。 應用程式程式碼仍會使用不同的標頭 X3DAUDIO。H 和 XPOFX。H，但現在會連結到單一的匯入程式庫，XAUDIO2 \_ 8.。
-   此版本的 XAudio2 無法使用 xWMA 支援;呼叫 CreateSourceVoice 時，不會將 xWMA 支援為音訊緩衝區格式。 我們現在建議媒體基礎的來源讀取器物件，將各種不同的媒體格式解碼成記憶體中的 PCM 緩衝區。
-   [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) 現在採用四個參數，而不是兩個。 較新的參數會在建立 [XAPOFX](xapofx-overview.md) 時指定初始資料。

## <a name="xaudio-27-and-earlier-windows-7"></a>XAudio 2.7 和舊版 (Windows 7) 

在應用程式中使用的所有舊版 XAudio2 都已提供為 DirectX SDK 中的可轉散發 Dll。 第一版的 XAudio2 （XAudio2 2.0）隨附于年3月2008版的 DirectX SDK。 DirectX SDK 中所提供的最後一個版本是 XAudio2 2.7，在2010年6月的 DirectX SDK 最後一版中提供。

由於已淘汰所有 SHA-1 簽署的內容，因此 Microsoft 下載不再提供舊版 DirectX SDK。 2010年6月是生命週期結束的版本。

舊版的 XAudio2 無法用來建立適用于 Windows 8 的 Windows Store 應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> <dt>

[XAudio2 重要概念](xaudio2-key-concepts.md)
</dt> </dl>

[XAudio 2.9 的可轉散發版本開發人員指南](xaudio2-redistributable.md)
</dt> </dl>
 

 
