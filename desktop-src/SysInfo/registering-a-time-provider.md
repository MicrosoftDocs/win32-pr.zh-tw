---
description: 系統會根據儲存在登錄中的設定資訊來載入時間提供者。
ms.assetid: 67f79c31-9dd7-4e3f-bfe1-701b10611f91
title: 註冊時間提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a98e5e516db6b2c800c917c5e47da9bd75ba5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849591"
---
# <a name="registering-a-time-provider"></a>註冊時間提供者

系統會根據儲存在登錄中的設定資訊來載入時間提供者。 每次提供者都應建立下列登錄機碼：

**HKEY \_LOCAL \_ MACHINE \\ System** \\ **CurrentControlSet** \\ **Services** \\ **W32Time** \\ **TimeProviders** \\ *ProviderName*

下表描述每個提供者的索引鍵中必須存在的值。



| 值             | 描述                                                                                                                                                                                                              |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DllName**       | 包含提供者之 DLL 的名稱。 此值的類型為 **REG \_ SZ**。                                                                                                                                     |
| **Enabled**       | 指出是否應啟動提供者。 如果這個值是1，則會啟動提供者。 否則，就不會啟動提供者。 此值的類型為 **REG \_ DWORD**。                                           |
| **InputProvider** | 指出提供者是否為輸入提供者或輸出提供者。 如果這個值是1，則提供者是輸入提供者。 否則，提供者就是輸出提供者。 此值的類型為 **REG \_ DWORD**。 |



 

時間提供者管理員會列舉 **TimeProviders** 索引鍵下的索引鍵，並啟動每個啟用的提供者。 提供者會在系統啟動時，以及每當有參數變更時啟動。

每次提供者也可以將應用程式特定的設定資訊儲存在登錄中。

 

 



