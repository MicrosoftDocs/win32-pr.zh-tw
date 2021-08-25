---
title: 使用者帳戶限制屬性集
description: 包含描述帳戶限制之使用者屬性的屬性集。
ms.assetid: 5616fede-12b1-41bd-b445-11c0e1ff66db
ms.tgt_platform: multiple
keywords:
- 使用者帳戶限制屬性集 AD 架構
topic_type:
- apiref
api_name:
- User-Account-Restrictions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050fe70f98bb0bb6fbb457e0540fa61bce9c8f61c2769cf24fb09aa87189d022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702718"
---
# <a name="user-account-restrictions-property-set"></a>使用者帳戶限制屬性集

包含描述帳戶限制之使用者屬性的屬性集。



| 進入 | 值 |
|--------------|--------------------------------------|
| CN           | 使用者帳戶-限制            |
| 顯示名稱 | 帳戶限制                 |
| 許可權-GUID  | 4c164200-20c0-11d0-a768-00aa006e0529 |



## <a name="implementations"></a>實作

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**亞當**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| 進入 | 值 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**使用者**](c-user.md)<br/> [**電腦**](c-computer.md)<br/>                                                                                                                                                   |
| 當地語系化-顯示識別碼 | 9                                                                                                                                                                                                                             |
| 屬性集成員    | [**帳戶-到期**](a-accountexpires.md)<br/> [**Pwd-上次設定**](a-pwdlastset.md)<br/> [**使用者帳戶控制**](a-useraccountcontrol.md)<br/> [**使用者參數**](a-userparameters.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| 進入 | 值 |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**使用者**](c-user.md)<br/> [**電腦**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| 當地語系化-顯示識別碼 | 9                                                                                                                                                                                                                                                                                                                            |
| 屬性集成員    | [**帳戶-到期**](a-accountexpires.md)<br/> [**ms-DS-使用者-帳戶-控制項計算**](a-msds-user-account-control-computed.md)<br/> [**Pwd-上次設定**](a-pwdlastset.md)<br/> [**使用者帳戶控制**](a-useraccountcontrol.md)<br/> [**使用者參數**](a-userparameters.md)<br/> |



## <a name="adam"></a>亞當



| 進入 | 值 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | \-                                                                                                                                                                                                    |
| 當地語系化-顯示識別碼 | 9                                                                                                                                                                                                     |
| 屬性集成員    | [**帳戶-到期**](a-accountexpires.md)<br/> [**ms-DS-使用者-帳戶-控制項計算**](a-msds-user-account-control-computed.md)<br/> [**Pwd-上次設定**](a-pwdlastset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| 進入 | 值 |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**使用者**](c-user.md)<br/> [**電腦**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                              |
| 當地語系化-顯示識別碼 | 9                                                                                                                                                                                                                                                                                                                            |
| 屬性集成員    | [**帳戶-到期**](a-accountexpires.md)<br/> [**ms-DS-使用者-帳戶-控制項計算**](a-msds-user-account-control-computed.md)<br/> [**Pwd-上次設定**](a-pwdlastset.md)<br/> [**使用者帳戶控制**](a-useraccountcontrol.md)<br/> [**使用者參數**](a-userparameters.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| 進入 | 值 |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**使用者**](c-user.md)<br/> [**電腦**](c-computer.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                                                                                                   |
| 當地語系化-顯示識別碼 | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 屬性集成員    | [**帳戶-到期**](a-accountexpires.md)<br/> [**ms-DS-使用者-帳戶-控制項計算**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-上次設定**](a-pwdlastset.md)<br/> [**使用者帳戶控制**](a-useraccountcontrol.md)<br/> [**使用者參數**](a-userparameters.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| 進入 | 值 |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**使用者**](c-user.md)<br/> [**電腦**](c-computer.md)<br/> [**ms DS 管理-服務-帳戶**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| 當地語系化-顯示識別碼 | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 屬性集成員    | [**帳戶-到期**](a-accountexpires.md)<br/> [**ms-DS-使用者-帳戶-控制項計算**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-上次設定**](a-pwdlastset.md)<br/> [**使用者帳戶控制**](a-useraccountcontrol.md)<br/> [**使用者參數**](a-userparameters.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| 進入 | 值 |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Applies-To              | [**使用者**](c-user.md)<br/> [**電腦**](c-computer.md)<br/> [**ms DS 管理-服務-帳戶**](c-msds-managedserviceaccount.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/>                                                                                                                                                                                                                  |
| 當地語系化-顯示識別碼 | 9                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| 屬性集成員    | [**帳戶-到期**](a-accountexpires.md)<br/> [**ms-DS-使用者-帳戶-控制項計算**](a-msds-user-account-control-computed.md)<br/> [**ms-DS-User-Password-Expiry-Time-Computed**](a-msds-userpasswordexpirytimecomputed.md)<br/> [**Pwd-上次設定**](a-pwdlastset.md)<br/> [**使用者帳戶控制**](a-useraccountcontrol.md)<br/> [**使用者參數**](a-userparameters.md)<br/> |



 

 





