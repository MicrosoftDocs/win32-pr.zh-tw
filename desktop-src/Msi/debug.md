---
description: 如果每一電腦的系統原則設定為 &\# 0034; 1&\# 0034;，則安裝程式會使用 OutputDebugString 函式，將一般的偵錯工具訊息寫入偵錯工具。
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: 偵錯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850247"
---
# <a name="debug"></a>偵錯

如果每一電腦的 [系統原則](system-policy.md) 設定為 "1"，則安裝程式會使用 [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) 函式，將一般的偵錯工具訊息寫入至偵錯工具。 如果這個值設定為 "2"，則安裝程式會使用 [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) 函式，將所有有效的偵錯工具訊息寫入至偵錯工具。 這項原則僅供偵測之用，在未來的 Windows Installer 版本中可能不受支援。

如果第三個 (0x04) 位是在 Debug 原則的值中設定，Windows Installer 只會將命令列寫入記錄檔。 因此，若要在記錄檔中顯示命令列，請將 [偵錯工具原則] 值設為 [7]。 這不會顯示與具有[密碼控制屬性](password-control-attribute.md)之[編輯控制項](edit-control.md)相關聯的屬性。 這會讓命令列上所設定的屬性，即使屬性包含在 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性中也一樣。 如需詳細資訊，請參閱 [防止機密資訊寫入至記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

 

 
