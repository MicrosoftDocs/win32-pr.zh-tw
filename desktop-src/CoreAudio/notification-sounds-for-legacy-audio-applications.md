---
description: 舊版音訊應用程式的通知聲音
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: 舊版音訊應用程式的通知聲音
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510612"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a>舊版音訊應用程式的通知聲音

在 Windows Vista 中，作業系統會將其所有的系統通知音效指派給跨進程音訊會話，該會話會透過目前指派給 eConsole [裝置角色](device-roles.md)的轉譯端點裝置播放。 系統音量控制程式 Sndvol 會顯示專用於系統通知音效的音量滑杆。

有些應用程式會播放通知聲音。 除了要求使用者透過 Sndvol 中的不同磁片區滑杆來管理應用程式的通知音效之外，應用程式也可以將其通知音效指派給與系統通知音效相同的會話。 控制系統通知音效的 Sndvol 音量滑杆，會控制應用程式的通知音效。

為了啟用此行為，Windows Vista 定義了 \_ 舊版 [**PlaySound**](/previous-versions//dd743680(v=vs.85)) 功能的 operators.snd 系統旗標。  (舊版 Windows 中不支援此旗標，包括 Windows Server 2003、Windows XP 及 Windows 2000 ) 。如果呼叫端設定此旗標，則 **PlaySound** 函式會將它所播放的音效指派給作業系統用於其通知音效的跨進程會話。 如果呼叫端未設定旗標，則 **PlaySound** 會將它所播放的音效指派給預設會話，也就是由會話 GUID 值 guid Null 所識別的進程特定會話 \_ 。 OPERATORS.SND \_ 系統定義于標頭檔 Mmsystem 中。 如需 **PlaySound** 的詳細資訊，請參閱 Windows SDK 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[與舊版音訊 Api 的互通性](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
