---
description: 系統存放區是由一或多個實體同級存放區所組成的集合。
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: 系統存放區位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944363"
---
# <a name="system-store-locations"></a>系統存放區位置

系統存放區是由一或多個實體同級存放區所組成的集合。 每個系統存放區都有預先定義的實體同級存放區。 開啟系統存放區（例如 MY at CERT \_ system \_ store 目前 \_ 的 \_ 使用者）之後，存放區提供者會呼叫 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 來開啟系統存放區集合中的每個實體存放區。 在開啟的進程中，每個實體存放區都會使用 [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)新增至系統存放區集合。 這些實體存放區中的所有憑證都可透過邏輯系統存放區集合使用。

針對每個系統存放區位置，預先定義的系統存放區為：

-   MY
-   Root
-   信任
-   CA

在 CERT \_ SYSTEM \_ STORE \_ 目前的 \_ 使用者中，也有預先定義的 UserDS 存放區。 已為此位置規劃智慧卡存放區。

以下是系統存放區，後面接著進一步的備註：

-   [CERT \_ 系統 \_ 存放區 \_ 目前的 \_ 使用者](#cert_system_store_current_user)
-   [CERT \_ 系統 \_ 存放區 \_ 本機 \_ 電腦](#cert_system_store_local_machine)
-   [CERT \_ 系統 \_ 存放區 \_ 目前的 \_ 服務](#cert_system_store_current_service)
-   [CERT \_ 系統 \_ 存放區 \_ 服務](#cert_system_store_services)
-   [CERT \_ 系統 \_ 存放區 \_ 使用者](#cert_system_store_users)
-   [CERT \_ 系統 \_ 目前的 \_ 使用者 \_ 組 \_ 策略](#cert_system_current_user_group_policy)
-   [CERT \_ 系統 \_ 本機 \_ 電腦 \_ 組 \_ 策略](#cert_system_local_machine_group_policy)
-   [CERT \_ SYSTEM \_ STORE \_ 本機 \_ 電腦 \_ ENTERPRISE](#cert_system_store_local_machine_enterprise)
-   [備註](#remarks)

### <a name="cert_system_store_current_user"></a>CERT \_ 系統 \_ 存放區 \_ 目前的 \_ 使用者

CERT \_ SYSTEM \_ STORE \_ 目前 \_ 的使用者系統存放區位於下列登錄位置：

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

與這些系統存放區相關聯的預先定義實體存放區如下所示。



| 系統存放區 | 實體存放區                                           |
|--------------|----------------------------------------------------------|
| MY           | .預設                                                 |
| Root         | .預設的 LocalMachine<br/> .智慧卡<br/>   |
| 信任        | .預設值。 GroupPolicy<br/> .My<br/> |
| CA           | .預設值。 GroupPolicy<br/> .My<br/> |
| UserDS       | .UserCertificate                                         |



 

### <a name="cert_system_store_local_machine"></a>CERT \_ 系統 \_ 存放區 \_ 本機 \_ 電腦

CERT \_ system \_ STORE \_ 本機 \_ 電腦系統存放區位於下列登錄位置：

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

預先定義的實體存放區會與這些系統存放區產生關聯，如下所示。



| 系統存放區 | 實體存放區                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| MY           | .預設                                                                                          |
| Root         | .預設值。 AuthRoot<br/> .GroupPolicy<br/> .企業<br/> .智慧卡<br/> |
| 信任        | .預設值。 GroupPolicy<br/> .企業<br/>                                            |
| CA           | .預設值。 GroupPolicy<br/> .企業 <br/>                                           |



 

### <a name="cert_system_store_current_service"></a>CERT \_ 系統 \_ 存放區 \_ 目前的 \_ 服務

CERT \_ SYSTEM \_ STORE \_ 目前 \_ 的服務系統存放區位於下列登錄位置：

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

與這些系統存放區相關聯的預先定義實體存放區如下所示。



| 系統存放區 | 實體存放區                   |
|--------------|----------------------------------|
| MY           | .預設                         |
| Root         | .預設的 LocalMachine<br/> |
| 信任        | .預設的 LocalMachine<br/> |
| CA           | .預設的 LocalMachine<br/> |



 

### <a name="cert_system_store_services"></a>CERT \_ 系統 \_ 存放區 \_ 服務

CERT \_ system \_ STORE \_ 服務系統存放區位於下列登錄位置：

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

與這些系統存放區相關聯的預先定義實體存放區如下所示。



| 系統存放區       | 實體存放區                   |
|--------------------|----------------------------------|
| ServiceName \\ MY    | .預設                         |
| ServiceName \\ 根目錄  | .預設的 LocalMachine<br/> |
| ServiceName \\ 信任 | .預設的 LocalMachine<br/> |
| ServiceName \\ CA    | .預設的 LocalMachine<br/> |



 

### <a name="cert_system_store_users"></a>CERT \_ 系統 \_ 存放區 \_ 使用者

CERT \_ system \_ STORE \_ 使用者的系統存放區位於下列登錄位置：

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

與這些系統存放區相關聯的預先定義實體存放區如下所示。



| 系統存放區  | 實體存放區                   |
|---------------|----------------------------------|
| userid \\ MY    | .預設的 LocalMachine<br/> |
| userid \\ 根  | .預設的 LocalMachine<br/> |
| userid \\ 信任 | .預設的 LocalMachine<br/> |
| userid \\ CA    | .預設的 LocalMachine<br/> |



 

### <a name="cert_system_current_user_group_policy"></a>CERT \_ 系統 \_ 目前的 \_ 使用者 \_ 組 \_ 策略

CERT \_ 系統 \_ 目前 \_ \_ 的使用者組 \_ 策略系統存放區位於下列登錄位置：

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a>CERT \_ 系統 \_ 本機 \_ 電腦 \_ 組 \_ 策略

CERT \_ 系統 \_ 本機 \_ 電腦 \_ 組 \_ 策略系統存放區位於下列登錄位置：

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a>CERT \_ SYSTEM \_ STORE \_ 本機 \_ 電腦 \_ ENTERPRISE

CERT \_ SYSTEM \_ STORE \_ 本機 \_ 電腦 \_ enterprise 包含企業內跨網域共用的憑證，並從全球企業目錄下載。 若要同步處理用戶端的企業存放區，企業目錄會每隔8小時輪詢一次，而且會在背景自動下載憑證。

與這些系統存放區相關聯的預先定義實體存放區如下所示。



| 系統存放區 | 實體存放區 |
|--------------|----------------|
| MY           | .預設       |
| Root         | .預設       |
| 信任        | .預設       |
| CA           | .預設       |



 

### <a name="remarks"></a>備註

您可以使用 [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)，將其他實體存放區與系統存放區相關聯。

Cert \_ 系統 \_ 存放區 \_ 服務和 cert \_ 系統 \_ 存放區使用者存放區的 \_ 開啟方式是在傳遞至 *pvPara* 的字串中，以服務或使用者名稱（例如 *ServiceName* \\ **信任** 或）來附加存放區的名稱 **。預設值** 是 \\ **MY**。 CERT \_ 系統 \_ 存放區 \_ 服務或憑證 \_ 系統 \_ 存放區 \_ 使用者位置可以 \_ \_ \_ \_ \_ \_ \_ 使用目前服務或使用者的文字 [*安全性識別*](../secgloss/s-gly.md) 元 (SID) ，開啟 cert system current SERVICE 或 cert system store 目前使用者中的相同存放區。

在 \_ \_ \_ \_ \_ \_ 電腦啟動或使用者登入期間，系統會在網路設定中，從群組原則範本 (GPT) ，將存放區的使用者群組原則和憑證系統 \_ 本機 \_ 電腦 \_ 組 \_ 策略下載到用戶端電腦。 當系統管理員在網域伺服器上變更 GPT 時，可以在啟動或登入之後，在用戶端電腦上更新這些存放區。 [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)函式可讓應用程式在其中一個位置的存放區變更時收到通知。

您可以從遠端開啟下列系統存放區位置：

-   CERT \_ 系統 \_ 存放區 \_ 本機 \_ 電腦
-   CERT \_ 系統 \_ 存放區 \_ 本機 \_ 電腦 \_ 組 \_ 策略
-   CERT \_ 系統 \_ 存放區 \_ 服務
-   CERT \_ 系統 \_ 存放區 \_ 使用者

系統存放區位置會從遠端開啟，方法是在傳遞至 *pvPara* 的字串中，將存放區名稱前面加上電腦名稱稱。 遠端系統存放區名稱的範例如下：

-   *ComputerName* \\**CA**
-   \\\\*ComputerName* \\**CA**
-   *ComputerName* \\*ServiceName* \\**信任**
-   \\\\*ComputerName* \\*ServiceName* \\**信任**

 

 
