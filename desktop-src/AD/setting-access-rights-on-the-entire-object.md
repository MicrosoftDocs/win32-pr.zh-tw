---
title: 設定整個物件的存取權限
description: 您只能針對整個物件（例如刪除和列出內容）設定某些許可權。 您也可以針對整個物件設定作業特定許可權（例如讀取權限），以便將它們套用至整個物件。
ms.assetid: 786357f4-146e-4638-8bd6-82bc1a6640a1
ms.tgt_platform: multiple
keywords:
- 設定整個物件 AD 的存取權限
- 物件 AD，設定存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a965b646de1ee3eba40757386fd243839cb35b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462817"
---
# <a name="setting-access-rights-on-the-entire-object"></a><span data-ttu-id="c06c0-106">設定整個物件的存取權限</span><span class="sxs-lookup"><span data-stu-id="c06c0-106">Setting Access Rights on the Entire Object</span></span>

<span data-ttu-id="c06c0-107">您只能針對整個物件（例如刪除和列出內容）設定某些許可權。</span><span class="sxs-lookup"><span data-stu-id="c06c0-107">Certain permissions can be set only for an entire object, such as Delete and List Contents.</span></span> <span data-ttu-id="c06c0-108">您也可以針對整個物件設定作業特定許可權（例如讀取權限），以便將它們套用至整個物件。</span><span class="sxs-lookup"><span data-stu-id="c06c0-108">Operation-specific permissions, such as the Read permission, can also be set for entire object so that they apply to an entire object.</span></span>

<span data-ttu-id="c06c0-109">您可以使用下列程式來設定整個物件的許可權。</span><span class="sxs-lookup"><span data-stu-id="c06c0-109">The following procedure can be used to set permissions for an entire object.</span></span>

<span data-ttu-id="c06c0-110">**若要設定整個物件的許可權**</span><span class="sxs-lookup"><span data-stu-id="c06c0-110">**To set permissions for an entire object**</span></span>

1.  <span data-ttu-id="c06c0-111">將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ADS \_ AceType \_ 存取 \_ 允許** 或 **ads \_ AceType \_ \_ 拒絕存取**。</span><span class="sxs-lookup"><span data-stu-id="c06c0-111">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED** or **ADS\_ACETYPE\_ACCESS\_DENIED**.</span></span>
2.  <span data-ttu-id="c06c0-112">將 [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 與 **IADsAccessControlEntry. InheritedObjectType** 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="c06c0-112">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) and **IADsAccessControlEntry.InheritedObjectType** to **NULL**.</span></span>

<span data-ttu-id="c06c0-113">如需有關如何建立 ACE 的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="c06c0-113">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="c06c0-114">如需可用於設定 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。</span><span class="sxs-lookup"><span data-stu-id="c06c0-114">For more information and a code example that can be used to set an ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 