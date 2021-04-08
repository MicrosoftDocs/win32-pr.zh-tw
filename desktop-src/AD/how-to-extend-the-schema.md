---
title: 如何延伸架構
description: 當現有的類別及/或屬性不符合您想要儲存的資料類型時，您可能會想要擴充架構。
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- 架構 AD，如何擴充
- Active Directory，使用架構
- Active Directory，使用、架構、延伸架構、如何擴充
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681656"
---
# <a name="how-to-extend-the-schema"></a><span data-ttu-id="e806b-106">如何延伸架構</span><span class="sxs-lookup"><span data-stu-id="e806b-106">How to Extend the Schema</span></span>

<span data-ttu-id="e806b-107">當現有的類別及/或屬性不符合您想要儲存的資料類型時，您可能會想要擴充架構。</span><span class="sxs-lookup"><span data-stu-id="e806b-107">When the existing classes and/or attributes do not fit with the type of data that you want to store, you might want to extend the schema.</span></span> <span data-ttu-id="e806b-108">如需有關如何決定何時延伸架構的詳細資訊，請參閱 [擴充架構](extending-the-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="e806b-108">For more information on deciding when to extend the schema, see [Extending the Schema](extending-the-schema.md).</span></span> <span data-ttu-id="e806b-109">當您決定需要架構延伸時，請使用下列程式來擴充架構。</span><span class="sxs-lookup"><span data-stu-id="e806b-109">When you have decided that schema extension is required, use the following procedure to extend the schema.</span></span>

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a><span data-ttu-id="e806b-110">套用任何架構延伸之前，請先確認 Active Directory 功能</span><span class="sxs-lookup"><span data-stu-id="e806b-110">Verify Active Directory functionality before you apply any schema extensions</span></span>

<span data-ttu-id="e806b-111">請先確認 Active Directory 功能，然後再更新架構，以協助確保架構延伸模組不會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="e806b-111">Verify Active Directory functionality before you update the schema to help ensure that the schema extension proceeds without error.</span></span> <span data-ttu-id="e806b-112">至少要確定樹系的所有網域控制站都在線上，並且執行輸入複寫。</span><span class="sxs-lookup"><span data-stu-id="e806b-112">At a minimum, ensure that all domain controllers for the forest are online and performing inbound replication.</span></span>

<span data-ttu-id="e806b-113">**若要在套用架構延伸之前確認 Active Directory 功能**</span><span class="sxs-lookup"><span data-stu-id="e806b-113">**To verify Active Directory functionality before you apply the schema extension**</span></span>

1.  <span data-ttu-id="e806b-114">登入已安裝 Windows 支援工具 Repadmin.exe 的系統管理工作站。</span><span class="sxs-lookup"><span data-stu-id="e806b-114">Log on to an administrative workstation that has the Windows Support Tool Repadmin.exe installed.</span></span>
    > [!Note]  
    > <span data-ttu-id="e806b-115">支援工具位於作業系統安裝媒體的 [支援 \\ 工具] 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="e806b-115">The Support Tools are located on the operating system installation media in the Support\\Tools folder.</span></span>

     

2.  <span data-ttu-id="e806b-116">開啟命令提示字元，然後將目錄變更為安裝 Windows 支援工具的資料夾。</span><span class="sxs-lookup"><span data-stu-id="e806b-116">Open a command prompt, and then change directories to the folder in which the Windows Support Tools are installed.</span></span>
3.  <span data-ttu-id="e806b-117">在命令提示字元輸入以下命令，然後按下 ENTER：</span><span class="sxs-lookup"><span data-stu-id="e806b-117">At a command prompt, type the following, and then press ENTER:</span></span>

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    <span data-ttu-id="e806b-118">所有網域控制站都應該在 [失敗] 資料行中顯示0，而最大的差異 (表示自上次) 成功複寫之後，對 Active Directory 資料庫所做的變更數目，應該小於或等於網域控制站用於複寫的站台連結的複寫頻率。</span><span class="sxs-lookup"><span data-stu-id="e806b-118">All domain controllers should show 0 in the Fails column, and the largest deltas (which indicate the number of changes that have been made to the Active Directory database since the last successful replication) should be less than or roughly equal to the replication frequency of the site link that is used by the domain controller for replication.</span></span> <span data-ttu-id="e806b-119">預設複寫頻率為180分鐘。</span><span class="sxs-lookup"><span data-stu-id="e806b-119">The default replication frequency is 180 minutes.</span></span>

    <span data-ttu-id="e806b-120">如需在套用架構延伸之前，您可以採取以確認 Active Directory 功能之其他步驟的詳細資訊，請參閱 [Microsoft 知識庫中的文章 325379](https://support.microsoft.com/kb/325379/en-us)。</span><span class="sxs-lookup"><span data-stu-id="e806b-120">For more information about additional steps that you can take to verify Active Directory functionality before you apply the schema extension, see [article 325379 in the Microsoft Knowledge Base](https://support.microsoft.com/kb/325379/en-us).</span></span>

<span data-ttu-id="e806b-121">**延伸架構**</span><span class="sxs-lookup"><span data-stu-id="e806b-121">**To Extend the Schema**</span></span>

1.  <span data-ttu-id="e806b-122">決定擴充方法。</span><span class="sxs-lookup"><span data-stu-id="e806b-122">Determine the method of extension.</span></span> <span data-ttu-id="e806b-123">當您仔細設計架構變更之後，下一步是決定要使用哪一種方法來擴充架構。</span><span class="sxs-lookup"><span data-stu-id="e806b-123">Once you have carefully designed your schema changes, the next step is to decide which method to use to extend the schema.</span></span> <span data-ttu-id="e806b-124">您可以使用下列其中一種方法：</span><span class="sxs-lookup"><span data-stu-id="e806b-124">You can use one of the following methods:</span></span>
    -   <span data-ttu-id="e806b-125">使用匯入檔案手動進行。</span><span class="sxs-lookup"><span data-stu-id="e806b-125">Manually, using import files.</span></span> <span data-ttu-id="e806b-126">請參閱 [使用 LDIFDE 工具](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))的檔。</span><span class="sxs-lookup"><span data-stu-id="e806b-126">See the documentation [Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65)).</span></span>
        > [!Note]  
        > <span data-ttu-id="e806b-127">請勿使用 LDIFDE 匯入 Windows .Sch \* .ldf 檔案。</span><span class="sxs-lookup"><span data-stu-id="e806b-127">Do not use LDIFDE to import Windows Sch\*.ldf files.</span></span> <span data-ttu-id="e806b-128">需要這些檔案才能延伸 Active Directory 的架構，以便安裝執行比目前架構主機上所執行之新版 Windows Server 的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="e806b-128">Those files are required to extend the Active Directory schema in order to install domain controllers that run a newer version of Windows Server than the version that is running on the current schema master.</span></span> <span data-ttu-id="e806b-129">當您需要擴充架構以便安裝新的網域控制站時，請使用 Adprep.exe。</span><span class="sxs-lookup"><span data-stu-id="e806b-129">When you need to extend the schema in order to install a new domain controller, use Adprep.exe.</span></span>

         

    -   <span data-ttu-id="e806b-130">以程式設計方式使用安裝程式。</span><span class="sxs-lookup"><span data-stu-id="e806b-130">Programmatically, using an installation program.</span></span> <span data-ttu-id="e806b-131">如需詳細資訊，請參閱程式 [設計延伸](programmatic-extension.md)</span><span class="sxs-lookup"><span data-stu-id="e806b-131">For more information, see [Programmatic Extension](programmatic-extension.md)</span></span>
2.  <span data-ttu-id="e806b-132">啟用架構變更。</span><span class="sxs-lookup"><span data-stu-id="e806b-132">Enable Schema Changes.</span></span> <span data-ttu-id="e806b-133">如需詳細資訊，請參閱 [安裝架構延伸的必要條件](prerequisites-for-installing-a-schema-extension.md) ，以及 [在架構主機上啟用架構變更](enabling-schema-changes-at-the-schema-master.md)。</span><span class="sxs-lookup"><span data-stu-id="e806b-133">For more information, see [Prerequisites for Installing a Schema Extension](prerequisites-for-installing-a-schema-extension.md) and [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
3.  <span data-ttu-id="e806b-134">取得新屬性和/或類別 (OID) 的物件識別碼，如 [取得物件識別碼](obtaining-an-object-identifier.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e806b-134">Obtain an Object Identifier (OID) for your new attributes and/or classes, as described in [Obtaining an Object Identifier](obtaining-an-object-identifier.md).</span></span>
4.  <span data-ttu-id="e806b-135">建立新的屬性和類別。</span><span class="sxs-lookup"><span data-stu-id="e806b-135">Create new attributes and classes.</span></span>
5.  <span data-ttu-id="e806b-136">如有必要，請使用顯示規範，將新的屬性和類別與使用者介面整合。</span><span class="sxs-lookup"><span data-stu-id="e806b-136">Use display specifiers to integrate new attributes and classes with the user interface, if necessary.</span></span>
6.  <span data-ttu-id="e806b-137">更新架構快取，如 [更新架構](updating-the-schema-cache.md)快取中所述。</span><span class="sxs-lookup"><span data-stu-id="e806b-137">Update the schema cache as described in [Updating the Schema Cache](updating-the-schema-cache.md).</span></span>
7.  <span data-ttu-id="e806b-138">使用 LDP.exe 來確認架構延伸。</span><span class="sxs-lookup"><span data-stu-id="e806b-138">Verify the schema extension using LDP.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e806b-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="e806b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e806b-140">取得物件識別碼</span><span class="sxs-lookup"><span data-stu-id="e806b-140">Obtaining an Object Identifier</span></span>](obtaining-an-object-identifier.md)
</dt> <dt>

[<span data-ttu-id="e806b-141">Windows Server 2003 中 Active Directory 的新命令列工具</span><span class="sxs-lookup"><span data-stu-id="e806b-141">The new command-line tools for Active Directory in Windows Server 2003</span></span>](https://support.microsoft.com/kb/298882)
</dt> <dt>

<span data-ttu-id="e806b-142">[使用 LDIFDE 工具](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span><span class="sxs-lookup"><span data-stu-id="e806b-142">[Using the LDIFDE Tool](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))</span></span>
</dt> <dt>

<span data-ttu-id="e806b-143">[擴充 Active Directory 架構](/previous-versions/ms806972(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="e806b-143">[Extending the Active Directory Schema](/previous-versions/ms806972(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="e806b-144">架構延伸的限制</span><span class="sxs-lookup"><span data-stu-id="e806b-144">Restrictions on Schema Extension</span></span>](restrictions-on-schema-extension.md)
</dt> </dl>

 

 