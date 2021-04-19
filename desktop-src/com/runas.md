---
title: RunAs
description: 當遠端用戶端未撰寫為服務應用程式時，將類別設定為在特定使用者帳戶下執行。
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- RunAs 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106965866"
---
# <a name="runas"></a>RunAs

當遠端用戶端未撰寫為服務應用程式時，將類別設定為在特定使用者帳戶下執行。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a>備註

值會指定使用者 *名稱，而且* 必須是 [使用者名稱]、[ *網域 ***\\*** 使用者* 名稱] 或 [互動式使用者] 字串格式。 您也可以指定 "nt 授權 \\ localservice" (用於本機服務) 和 "nt 授權 \\ networkservice" (For Network service) 。 \\當 {*AppID \_ GUID*} 參考到已啟動或在類別資料表中有專案的 COM 伺服器時，您也可以指定 "nt 授權單位系統" 字串。 不過，您無法使用「nt 授權單位系統」搭配 \\ 尚未啟動的 COM 伺服器。 "Nt 授權單位 \\ localservice"、"nt 授權單位 \\ networkservice" 和 "nt 授權單位系統" 的預設密碼 \\ 為 "" (空白字串) 。

> [!Note]  
> 從 Windows Vista，您不再需要使用空白密碼來設定 "nt 授權單位 \\ localservice"、"nt 授權單位 \\ networkservice" 和 "nt 授權單位 \\ 系統" **RunAs** 設定。

 

設定為以特定使用者身分執行的類別可能無法在任何其他身分識別下註冊，因此使用此 CLSID 的 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) 呼叫會失敗，除非 COM 會代表實際的啟用要求啟動進程。

使用者名稱是取自類別的 **AppID** 金鑰底下的 **RunAs** 值。 如果使用者名稱為「互動式使用者」，則會以目前登入之使用者的身分識別來執行伺服器，並連接到互動式桌面。

否則，系統會從登錄的一部分取出密碼，而這部分只適用于電腦的系統管理員和系統的系統管理員。 然後，使用者名稱和密碼會用來建立伺服器執行所在的登入會話。 以這種方式啟動時，使用者會使用自己的桌面和視窗來執行，且不會與互動式使用者或其他使用者帳戶中執行的其他使用者共用視窗控制碼、剪貼簿或其他 UI 元素。

若要建立 **RunAs** 類別的密碼，您必須使用安裝在系統目錄中的 DCOMCNFG 系統管理工具。

針對 DCOM 伺服器所使用的 **RunAs** 身分識別，值中所指定的使用者帳戶必須具有以批次工作登入的許可權。 您可以使用「本機安全性原則」系統管理工具來新增此許可權。 移至 [ **本機原則** ]，並開啟 [ **使用者權限指派**]。 選取 [ **以批次工作登** 入]，然後新增使用者帳戶。

**RunAs** 值不會用於設定要以服務方式執行的伺服器。 需要以 LocalSystem 以外的身分識別執行的 COM 服務應該使用服務控制台小程式或服務控制器功能來設定適當的使用者名稱和密碼。  (如需這些函式的詳細資訊，請參閱 [服務](/windows/desktop/Services/services)。 ) 

> [!Note]  
> 從 Microsoft Windows Server 2003 開始，類別 AppID 會明確地從 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ appid**（不同于大部分的登錄機碼）進行讀取，而無法與 **HKEY \_ 類別 \_ 根目錄 \\ appid** 交換。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 伺服器](registering-com-servers.md)
</dt> </dl>

 

 