---
title: 其他與 Microsoft Agent 相容的語音引擎
description: 其他與 Microsoft Agent 相容的語音引擎
ms.assetid: fa87c592-c819-4dea-a1d0-6ccb25cc0bcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9855a0f5374d35634d02f808b46449a053cada9a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374630"
---
# <a name="other-speech-engines-compatible-with-microsoft-agent"></a>其他與 Microsoft Agent 相容的語音引擎

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

除了隨附于和支援 Microsoft Agent 的 Microsoft 語音引擎之外，許多公司也提供支援 Microsoft 代理程式的語音引擎。 此頁面提供這類引擎的簡短總覽，這些引擎可能會以美式英文和其他語言提供。 如需有關如何安裝和存取，以及授權和轉散發引擎的資訊，請參閱其網站。

使用任何協力廠商語音引擎時，您也必須安裝 Microsoft SAPI 4.0 執行時間二進位檔，才能正確列舉引擎。 您可以從網頁加入下列標記，以觸發語音 API 的 autodownload：

``` syntax
<OBJECT WIDTH=0 HEIGHT=0
  CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
  CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

如需有關 SAPI 執行時間二進位檔的詳細資訊，請參閱 [Microsoft Speech group 的網站](https://msdn.microsoft.com/library/ee705648.aspx)。 Microsoft 代理程式也會使用 Microsoft 語音辨識引擎、語音主控台和代理程式字元編輯器來安裝 SAPI 執行時間二進位檔。

請注意，這些連結指向不在 Microsoft control 下的伺服器。 請閱讀有關其他伺服器的 Microsoft [官方聲明](https://www.microsoft.com/isapi/gomscom.asp?TARGET=/Misc/NonMS.md) 。 Microsoft 不會為這些網站上的內容或軟體提供背書。 所有技術和支援問題也應導向至引擎供應商，而不是 Microsoft 或 Microsoft 代理商團隊。

**Digalo 文字轉換語音引擎**

Digalo 是為使用者和開發人員設計的實惠 TTS 引擎。 引擎提供多種語言：法文、德文、葡萄牙文 (巴西) 、西班牙文、俄文、英國和美式英文，且即將推出義大利文、波蘭文和其他語言。 此外，也提供了開發人員資訊，以及使用者註冊和分支機搆方案的詳細資料。

**Elan 語音引擎**

Elan 語音引擎使用 Elan 的文字轉換語音技術，並提供七種語言：法文、德文、葡萄牙文 (巴西) 、西班牙文、俄文、英國和美國英文。

**IBM ViaVoice Outloud**

IBM 已開發了數個 Microsoft 代理程式字元，可搭配 ViaVoice Outloud 使用。 IBM ViaVoice Outloud 是一種文字轉換語音 (語音合成) 技術，並提供法文、德文、義大利文、西班牙文、UK 和美式英文。 結合 Microsoft Agent 時，您可以使用多種語言建立活躍的應用程式，並將銷售商機延伸至新的全球市場。

 

 




