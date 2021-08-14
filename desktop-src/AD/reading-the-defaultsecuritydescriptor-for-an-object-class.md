---
title: 讀取物件類別的 defaultSecurityDescriptor
description: 您可以使用 ADSI 取得具有 IADs 介面之物件類別的 defaultSecurityDescriptor 屬性。
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，讀取物件類別的 defaultSecurityDescriptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26204ebe31155363a1be8bf30bd1c0495d16a939b58789f421a0772d6d90a9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184689"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a>讀取物件類別的 defaultSecurityDescriptor

您可以使用 ADSI 取得具有 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)介面之物件類別的 **defaultSecurityDescriptor** 屬性。 若要取得物件類別的 **defaultSecurityDescriptor** 屬性，請執行下列步驟。

1.  取得物件類別之 **classSchema** 物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)介面指標。
2.  使用 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-get) 取得物件的預設安全描述項。 包含安全描述項的屬性名稱為 "defaultSecurityDescriptor"。 屬性將會傳回為 [**變數**](/windows/win32/api/oaidl/ns-oaidl-variant) ，其包含具有 SDDL 字串格式之預設安全描述項的 BSTR。
3.  您可以使用 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 函式，將 SDDL 字串形式轉換成安全描述項。
4.  使用 [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)、 [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)、 [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)和 [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) 安全性 api 來讀取安全描述項的部分。

如需示範如何進行此作業的程式碼範例，請參閱 [閱讀 defaultSecurityDescriptor 的範例程式碼](example-code-for-reading-defaultsecuritydescriptor.md)。

 

 