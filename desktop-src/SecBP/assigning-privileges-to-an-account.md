---
description: 您可以使用本機安全性原則 Microsoft Management Console (MMC) 嵌入式管理單元 () Secpol.msc 或呼叫 LsaAddAccountRights 函式，將許可權指派給帳戶。
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: 將許可權指派給帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ba4fb5266a66aac67b17c70fc6bbcaa1a397a8593534144c688daaee5a0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623008"
---
# <a name="assigning-privileges-to-an-account"></a>將許可權指派給帳戶

您可以使用本機安全性原則 Microsoft Management Console (MMC) 嵌入式管理單元 () Secpol.msc 或呼叫 [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) 函式，將許可權指派給帳戶。

將許可權指派給帳戶並不會影響現有的使用者權杖。 使用者必須登出再重新登入，才能取得具有新指派許可權的存取權杖。

若要使用 [本機安全性原則] MMC 嵌入式管理單元指派許可權，請編輯 [**安全性設定/Local 原則/使用者權限指派**] 底下列出的每個許可權的使用者清單。

 

 
