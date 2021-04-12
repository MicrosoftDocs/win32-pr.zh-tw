---
description: 資源保護可防止取代作業系統檔案和資料夾，以及作業系統的必要登錄機碼。 修改受保護的資源可能會導致應用程式或系統失敗。
ms.assetid: 27df9300-8bea-4748-9acd-2c1625093ece
title: Windows 資源保護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff6c89e99b885256c7dd054a12c6a69795d794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319863"
---
# <a name="windows-resource-protection"></a>Windows 資源保護

## <a name="purpose"></a>目的

Windows 資源保護 (WRP) 可防止取代安裝為作業系統一部分的基本系統檔案、資料夾和登錄機碼。 從 Windows Server 2008 和 Windows Vista 開始，就可以開始使用。 應用程式不應覆寫這些資源，因為系統和其他應用程式會使用這些資源。 保護這些資源可防止應用程式和作業系統失敗。 WRP 是 Windows 檔案保護 (WFP) 的新名稱。 WRP 可保護登錄機碼和資料夾，以及基本的系統檔案。

## <a name="where-applicable"></a>適用時

所有以 Windows 為基礎的應用程式及其在 Windows Server 2008 或 Windows Vista 及更新版本作業系統上執行的安裝程式，都應該要知道 WRP。 所有在 Microsoft Windows Server 2003 或 Windows XP 上執行的 Windows 應用程式，以及其安裝程式，都應該要知道 WFP。

## <a name="developer-audience"></a>開發人員對象

WRP API 是設計來供 C/c + + 程式設計人員使用。 WRP API 有兩個函式： [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) 和 [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected)。

## <a name="run-time-requirements"></a>執行階段需求求

只使用 [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) 功能的應用程式需要 windows server 2008、windows Vista、windows server 2003 或 windows XP。 使用 [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected) 功能的應用程式需要 windows Server 2008 或 windows Vista。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                     | 描述                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------|
| [關於 Windows 資源保護](about-windows-file-protection.md)<br/>         | 關於 WRP 的一般資訊。<br/>   |
| [Windows 資源保護參考](windows-file-protection-reference.md)<br/> | WRP 的參考檔。<br/> |



 

 

 




