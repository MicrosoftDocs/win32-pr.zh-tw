---
title: 自訂配置登錄設定
description: 自訂配置登錄設定
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player，自訂配置登錄設定
- Windows Media Player，架構
- Windows Media Player，登錄
- 登錄，自訂配置設定
- 登錄，配置
- 登錄，Windows Media Player 的設定
- 配置
- 自訂配置登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1f20b69570a18d256049bb0e785099e43b091d080e4f9f65e62655c3103d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750391"
---
# <a name="custom-scheme-registry-settings"></a>自訂配置登錄設定

配置是自訂的通訊協定。 Windows Media Player 會維護使用者電腦上登錄中的配置清單。 當使用者嘗試播放數位媒體檔案時，播放者會先檢查 Windows 媒體格式 SDK 是否支援該配置。 如果不是，則播放清單會根據登錄中的清單來檢查配置。 如果找到相符的值，播放程式就會檢查指出哪些基礎技術或 *運行* 時間 (（例如 Microsoft DirectShow 或 Windows 媒體格式 SDK) ）可以用來播放檔案的值。 如果找不到相符項，播放程式會向使用者呈現警告對話方塊，提示使用者嘗試播放該檔案的許可權。 如果您使用自訂通訊協定配置串流數位媒體檔案，您可以註冊配置並提供執行時間的值，以防止此警告出現在使用者的電腦上。

配置清單會以一組符合已註冊配置的登錄機碼來維護，而不含冒號和兩個斜線 (：//) 。 例如，用來串流豐富媒體的 wmhtml://配置金鑰，名為 "wmhtml"。 針對本機電腦和每個使用者都可以維護個別的清單。 針對本機電腦，配置索引鍵是下列登錄機碼的子機碼：

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 架構\\**

例如，本機電腦的 wmhtml://配置機碼為：

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 配置 \\ wmhtml**

若要變更此機碼中的值或建立新的子機碼，目前的使用者必須是電腦的系統管理員。

針對個別使用者，配置索引鍵是下列登錄機碼的子機碼：

**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ Player \\ 方案\\**

例如，目前使用者的 wmhtml://配置索引鍵為：

**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ Player \\ 方案 \\ wmhtml**

檢查已註冊的配置時，播放程式會先檢查位於 **HKEY \_ 本機 \_ 電腦** 中的值。 如果找不到目前配置的任何值，則播放程式會接著檢查 **HKEY \_ 目前 \_ 使用者** 中的值。 如果找不到目前配置的任何內容，播放程式會向使用者顯示警告。

每個配置子機碼可能包含下列 *運行* 時間的其中一個可能值。



| 值 | 描述                                |
|-------|--------------------------------------------|
| 6     | 使用 Windows 媒體格式 SDK 轉譯。 |
| 7     | 使用 Microsoft DirectShow 呈現。         |



 

變更 Windows 媒體格式 SDK 支援的配置 *運行* 時間值將不會有任何作用。 播放程式一律會使用 Windows 媒體格式 sdk 作為 Windows 媒體格式 sdk 所支援的配置執行時間。 此登錄值是設計來允許自訂配置的執行時間設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**登錄設定**](registry-settings.md)
</dt> </dl>

 

 




