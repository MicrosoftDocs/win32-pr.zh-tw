---
description: SelfReg 資料表包含需要自行註冊之模組的相關資訊。
ms.assetid: 7fe5c96e-16a4-49c9-9a93-616608aa55b2
title: SelfReg 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5895b1d23369a7c121547fed841731b5d3e76ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695404"
---
# <a name="selfreg-table"></a>SelfReg 資料表

SelfReg 資料表包含需要自行註冊之模組的相關資訊。 安裝程式會在安裝模組期間呼叫 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 函式;它會在模組的卸載期間呼叫 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 。 安裝程式不會自行註冊 EXE 檔案。

SelfReg 資料表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| 檔案\_ | [識別碼](identifier.md) | Y   | N        |
| 成本   | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>檔\_
</dt> <dd>

在 [檔資料表](file-table.md) 的第一個資料行中的外部索引鍵，表示需要註冊的模組。

</dd> <dt>

<span id="Cost"></span><span id="cost"></span><span id="COST"></span>成本
</dt> <dd>

註冊模組的成本（以位元組為單位）。 此值必須是非負數。

</dd> </dl>

## <a name="remarks"></a>備註

使用自我註冊時，強烈建議使用安裝套件作者。 相反地，他們應針對此目的撰寫一或多個安裝程式所提供的資料表來註冊模組。 如需詳細資訊，請參閱登錄 [資料表群組](registry-tables-group.md)。 擁有集中式安裝程式服務的許多優點會因為自我註冊而遺失，因為自我註冊常式通常會隱藏重要的設定資訊。 避免自行註冊的原因包括：

-   您無法使用 [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) 來安全地復原具有自我註冊模組的安裝，因為沒有辦法告知是否有其他功能或應用程式使用自行註冊的金鑰。
-   如果在自我註冊常式內執行類別或延伸模組伺服器註冊，就會降低使用公告的能力。
-   安裝程式會針對每個使用者或每一部電腦的安裝，自動處理登錄資料表中的 HKCR 機碼。 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 常式目前不支援每個使用者 HKCR 索引鍵的概念。
-   如果有多個使用者在同一部電腦上使用自我註冊的應用程式，則每位使用者在第一次執行應用程式時都必須安裝該應用程式。 否則，安裝程式無法輕易判斷是否有適當的 HKCU 登錄機碼存在。
-   如果元件同時指定為從來源執行，而且列于 SelfReg 資料表中，則 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 可能會被拒絕存取網路資源（例如類型程式庫）。 這可能會導致元件的安裝在系統管理安裝期間失敗。
-   自我註冊 Dll 更容易撰寫程式碼錯誤，因為每個 DLL 的 [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) 所需的新程式碼通常都不同。 相反地，請使用資料庫中的登錄資料表來利用安裝程式所提供的現有程式碼。
-   自我註冊 Dll 有時可以連結至不存在或版本錯誤的輔助 Dll。 相反地，安裝程式可以使用登錄資料表註冊 Dll，而不會相依于系統目前的狀態。

> [!Note]  
> 您無法使用 [SelfRegModules](selfregmodules-action.md) 和 [SelfUnRegModules](selfunregmodules-action.md) 動作來指定安裝程式註冊或取消註冊自行註冊 dll 的順序。 請參閱 [指定自行註冊的順序](specifying-the-order-of-self-registration.md)。

 

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 
