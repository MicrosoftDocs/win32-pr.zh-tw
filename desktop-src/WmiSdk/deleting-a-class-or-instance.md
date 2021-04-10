---
description: 當您完成類別或實例之後，您可能想要從 WMI 刪除該類別或實例。
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: 刪除類別或實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192200"
---
# <a name="deleting-a-class-or-instance"></a><span data-ttu-id="bb376-103">刪除類別或實例</span><span class="sxs-lookup"><span data-stu-id="bb376-103">Deleting a Class or Instance</span></span>

<span data-ttu-id="bb376-104">當您完成類別或實例之後，您可能想要從 WMI 刪除該類別或實例。</span><span class="sxs-lookup"><span data-stu-id="bb376-104">After you finish with a class or an instance, you may wish to delete that class or instance from WMI.</span></span> <span data-ttu-id="bb376-105">如同其他物件導向技術，您可以刪除類別或實例物件來清除 WMI 命名空間，並傳回系統資源。</span><span class="sxs-lookup"><span data-stu-id="bb376-105">Like other object-oriented technologies, you can delete class or instance objects to clean up the WMI namespace and to return system resources.</span></span> <span data-ttu-id="bb376-106">不過，WMI 中的許多類別和實例都是持續性的，而且在任何指定的時間都是由各種應用程式使用，因此在刪除 WMI 類別或實例時，您應該要特別小心：您的應用程式或其他應用程式可能會在稍後的日期需要類別或實例。</span><span class="sxs-lookup"><span data-stu-id="bb376-106">However, many classes and instances in WMI are persistent and are used by a variety of applications at any given time Therefore, you should be careful when deleting a WMI class or instance: your application or another application will probably need the class or instance at a later date.</span></span>

<span data-ttu-id="bb376-107">刪除類別或實例是一個簡單的程式。</span><span class="sxs-lookup"><span data-stu-id="bb376-107">Deleting a class or an instance is a simple procedure.</span></span> <span data-ttu-id="bb376-108">不過，由於類別的永久本質，您可能不需要經常刪除某個類別。</span><span class="sxs-lookup"><span data-stu-id="bb376-108">However, due to the permanent nature of a class, you will probably not need to delete a class often.</span></span> <span data-ttu-id="bb376-109">例如，您不太可能刪除 [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) 類別，因為您不太可能在企業中的某處沒有磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bb376-109">For example, you are unlikely to delete the [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) class, because it is unlikely that you do not have a disk drive somewhere in your enterprise.</span></span> <span data-ttu-id="bb376-110">相反地，您會更有可能刪除類別的實例。</span><span class="sxs-lookup"><span data-stu-id="bb376-110">Instead, you will be more likely to delete an instance of a class.</span></span> <span data-ttu-id="bb376-111">如需詳細資訊，請參閱 [刪除實例](deleting-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="bb376-111">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span>

<span data-ttu-id="bb376-112">雖然很罕見，但您可能會在一段時間內需要更新所建立的類別。</span><span class="sxs-lookup"><span data-stu-id="bb376-112">Although uncommon, you may come across a time where you wish to update a class that you created.</span></span> <span data-ttu-id="bb376-113">例如，您可以建立類別來代表協力廠商應用程式。</span><span class="sxs-lookup"><span data-stu-id="bb376-113">For example, you could create a class to represent a third-party application.</span></span> <span data-ttu-id="bb376-114">如果協力廠商將其軟體更新至您的類別不再正確地表示軟體的範圍，您可能需要刪除原始類別。</span><span class="sxs-lookup"><span data-stu-id="bb376-114">If the third-party updated their software to the extent that your class no longer properly represented the software, you may need to delete your original class.</span></span> <span data-ttu-id="bb376-115">如需詳細資訊，請參閱 [刪除類別](deleting-a-class.md)。</span><span class="sxs-lookup"><span data-stu-id="bb376-115">For more information, see [Deleting a Class](deleting-a-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb376-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb376-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb376-117">設計受控物件格式 (MOF) 類別</span><span class="sxs-lookup"><span data-stu-id="bb376-117">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
