---
description: 核心音訊 Api
ms.assetid: 87ca9a31-1bc8-47ea-be00-40159d30e189
title: 核心音訊 Api
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 2cabb462d13786c874401394fa814484f79b0e3b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548953"
---
# <a name="core-audio-apis"></a>核心音訊 Api

> [!NOTE]
> 如需程式碼範例，請參閱 [使用核心音訊 api 的 SDK 範例](./sdk-samples-that-use-the-core-audio-apis.md)。

本檔提供適用于 Microsoft Windows 系列作業系統的核心音訊應用程式開發介面 (Api) 的相關資訊。 它提供軟體發展人員在開發使用 Windows Vista 中核心音訊 Api 的應用程式時所遵循的指導方針。 這些 Api 是 Windows Vista 中的新功能，不適用於舊版的 Windows。

核心音訊 Api 提供聲音應用程式存取音訊端點裝置的方法，例如耳機和麥克風。 核心音訊 Api 可作為較高層級音訊 Api 的基礎，例如 Microsoft DirectSound 和 Windows 多媒體 **waveXxx** 功能。 大部分的應用程式都會與較高層級的 Api 通訊，但有些具有特殊需求的應用程式可能需要直接與核心音訊 Api 通訊。

從 Windows 7 開始，已改善現有的 Api，並新增了新的 Api 來支援新案例。 串流和會話管理 Api 已經過改良，因此應用程式現在可以對音訊會話進行列舉和擴充控制。 藉由使用新的 Api，應用程式可以執行自訂的串流衰減體驗。 新裝置相關的 Api 可讓您存取端點裝置的驅動程式屬性。

本檔包含下列各節。

| 區段                                                                    | 描述                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [關於 Windows Core 音訊 Api](about-the-windows-core-audio-apis.md) | 提供 Windows core 音訊 Api 的總覽，並說明基本概念。 |
| [程式設計指南](programming-guide.md)                                 | 描述核心音訊 Api 的主要功能，以及如何使用它們。            |
| [程式設計參考](programming-reference.md)                         | 提供核心音訊 Api 的 c + + 參考資訊。                       |

## <a name="related-topics"></a>相關主題

[適用于 Windows 的媒體技術](/previous-versions/bg125389(v=msdn.10))

[使用核心音訊 Api 的 SDK 範例](./sdk-samples-that-use-the-core-audio-apis.md)