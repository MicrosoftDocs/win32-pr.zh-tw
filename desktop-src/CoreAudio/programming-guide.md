---
description: 瞭解 Windows Vista 核心音訊 api 的概念和功能，以及如何在應用程式設計中使用它們。
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: 核心音訊程式設計指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2b8f65d0c5508cd821b49a42b4b89ea42859390913a30534319d5ef7c79224f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088388"
---
# <a name="core-audio-programming-guide"></a>核心音訊程式設計指南

本指南章節將說明 Windows Vista 核心音訊 api 的概念和功能，並說明如何在應用程式設計中使用它們。

此章節包含下列主題。



| 主題                                                                                                                      | 描述                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [使用者模式音訊元件](user-mode-audio-components.md)                                                               | 透過核心音訊 Api 中的低層級介面，用戶端可以存取管理和混合音訊串流的系統元件。                                                                        |
| [受保護的使用者模式音訊 (PUMA) ](protected-user-mode-audio--puma-.md)                                                   | 描述受保護使用者模式音訊 (PUMA) 的更新，此為受保護環境中的使用者模式音訊引擎 (PE) ，可提供更安全的音訊處理和轉譯環境。              |
| [音訊端點裝置](audio-endpoint-devices.md)                                                                       | 音訊端點裝置是一種軟體抽象概念，可讓使用者輕鬆地與音訊裝置（例如麥克風和喇叭）互動。                                                              |
| [音訊會話](audio-sessions.md)                                                                                       | 音訊會話是一種軟體抽象概念，可讓用戶端將相關音訊串流的集合當作單一單位來管理。                                                                           |
| [音量控制項](volume-controls.md)                                                                                     | 系統會以邏輯一致的方式，將其以原則為基礎的磁片區設定與使用者的磁片區設定整合。                                                                                      |
| [串流管理](stream-management.md)                                                                                 | Windows 音訊會話 API (WASAPI) 提供用戶端一組完整的方法來建立和管理音訊串流。                                                                             |
| [裝置拓撲](device-topologies.md)                                                                                 | DeviceTopology API 可讓用戶端探索音訊硬體中不同資料路徑的音訊控制項。                                                                          |
| [使用 IKsControl 介面存取音訊屬性](using-the-ikscontrol-interface-to-access-audio-properties.md) | 特製化的音訊應用程式可能需要使用 IKsControl 介面來存取音訊介面卡的屬性。                                                                                     |
| [與舊版音訊 Api 的互通性](interoperability-with-legacy-audio-apis.md)                                     | Windows Vista 中核心音訊 api 的主要功能，可以整合到使用 DirectSound、DirectShow 和 Windows 多媒體 **waveOutXxx** 和 **waveInXxx** 功能的現有應用程式中。 |
| [空間音效](spatial-sound.md)                                                                                         | 提供在 Xbox 和 Windows 上使用 Windows Sonic、Microsoft 的平台層級解決方案來提供空間音效支援的指引，同時在接聽程式上方或下方啟用環繞和提高許可權 () 音訊提示。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[核心音訊 Api](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



