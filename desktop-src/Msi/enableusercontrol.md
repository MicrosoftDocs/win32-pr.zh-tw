---
description: 每一電腦的系統原則可用來指定 Windows Installer 在使用較高許可權的受控安裝期間，將所有公用屬性傳遞至伺服器端。
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114569"
---
# <a name="enableusercontrol"></a>EnableUserControl

在受控安裝的情況下，封裝作者可能需要限制哪些公用屬性會傳遞至伺服器端，並且可由非系統管理員的使用者進行變更。 當安裝要求安裝程式需要使用較高的許可權時，通常需要一些限制才能維護安全的環境。

如果每一電腦的 [系統原則](system-policy.md) 設定為 "1"，則安裝程式可以在使用較高許可權的受控安裝期間，將所有 [公用屬性](public-properties.md) 傳遞至伺服器端。 設定此原則的效果與設定 **EnableUserControl** 屬性相同。 設定此原則可讓所有公用屬性都傳遞至服務，並由非管理員使用者進行變更。 依預設，不會啟用此原則;只有受限制的公用屬性會傳遞至伺服器端，並由非系統管理員的使用者進行變更。 所有其他公用屬性都會被忽略。

如果作業系統是 Windows 2000、使用者不是系統管理員，而且應用程式或產品是以較高的許可權安裝，則不是系統管理員的使用者只能覆寫受限制公用屬性的核准清單。 如需詳細資訊，請參閱 [限制的公用屬性](restricted-public-properties.md)。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

 

 



