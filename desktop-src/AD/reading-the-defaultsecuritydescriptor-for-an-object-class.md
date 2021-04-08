---
title: 讀取物件類別的 defaultSecurityDescriptor
description: 您可以使用 ADSI 取得具有 IADs 介面之物件類別的 defaultSecurityDescriptor 屬性。
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，讀取物件類別的 defaultSecurityDescriptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023224"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a><span data-ttu-id="7ffa6-104">讀取物件類別的 defaultSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="7ffa6-104">Reading the defaultSecurityDescriptor for an Object Class</span></span>

<span data-ttu-id="7ffa6-105">您可以使用 ADSI 取得具有 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)介面之物件類別的 **defaultSecurityDescriptor** 屬性。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-105">Using ADSI, you can obtain the **defaultSecurityDescriptor** attribute for an object class with the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="7ffa6-106">若要取得物件類別的 **defaultSecurityDescriptor** 屬性，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-106">To obtain the **defaultSecurityDescriptor** attribute for an object class, perform the following steps.</span></span>

1.  <span data-ttu-id="7ffa6-107">取得物件類別之 **classSchema** 物件的 [**IADs**](/windows/desktop/api/iads/nn-iads-iads)介面指標。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-107">Get an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface pointer to the **classSchema** object for the object class.</span></span>
2.  <span data-ttu-id="7ffa6-108">使用 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-get) 取得物件的預設安全描述項。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-108">Use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to get the default security descriptor of the object.</span></span> <span data-ttu-id="7ffa6-109">包含安全描述項的屬性名稱為 "defaultSecurityDescriptor"。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-109">The name of the property that contains the security descriptor is "defaultSecurityDescriptor".</span></span> <span data-ttu-id="7ffa6-110">屬性將會傳回為 [**變數**](/windows/win32/api/oaidl/ns-oaidl-variant) ，其包含具有 SDDL 字串格式之預設安全描述項的 BSTR。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-110">The property will be returned as a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) containing a BSTR with the default security descriptor in SDDL string format.</span></span>
3.  <span data-ttu-id="7ffa6-111">您可以使用 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) 函式，將 SDDL 字串形式轉換成安全描述項。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-111">Use the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL string form to a security descriptor.</span></span>
4.  <span data-ttu-id="7ffa6-112">使用 [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl)、 [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl)、 [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)和 [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) 安全性 api 來讀取安全描述項的部分。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-112">Use the [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner), and [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Security APIs to read the parts of the security descriptor.</span></span>

<span data-ttu-id="7ffa6-113">如需示範如何進行此作業的程式碼範例，請參閱 [閱讀 defaultSecurityDescriptor 的範例程式碼](example-code-for-reading-defaultsecuritydescriptor.md)。</span><span class="sxs-lookup"><span data-stu-id="7ffa6-113">For a code example that demonstrates how to do this, see [Example Code for Reading defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span></span>

 

 