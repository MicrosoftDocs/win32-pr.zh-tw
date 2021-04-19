---
description: 在 WMI 中，類別是一種物件，可描述企業的某些層面，例如特殊類型的磁片磁碟機。
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: 建立 WMI 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985335"
---
# <a name="creating-a-wmi-class"></a><span data-ttu-id="4079e-103">建立 WMI 類別</span><span class="sxs-lookup"><span data-stu-id="4079e-103">Creating a WMI Class</span></span>

<span data-ttu-id="4079e-104">在 WMI 中，類別是一種物件，可描述企業的某些層面，例如特殊類型的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="4079e-104">In WMI, a class is an object that describes some aspect of an enterprise, such as a special type of disk drive.</span></span> <span data-ttu-id="4079e-105">建立類別定義之後，請撰寫您的提供者 DLL，以提供類別的實例、屬性資料，以及針對該類別定義的執行方法。</span><span class="sxs-lookup"><span data-stu-id="4079e-105">After you have created a class definition, write your provider DLL to supply instances of the class, property data, and execute methods defined for the class.</span></span> <span data-ttu-id="4079e-106">然後，腳本和應用程式可以取得資料或控制裝置。</span><span class="sxs-lookup"><span data-stu-id="4079e-106">Scripts and applications can then obtain data or control the device.</span></span> <span data-ttu-id="4079e-107">如需詳細資訊，請參閱 [開發 WMI 提供者](developing-a-wmi-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="4079e-107">For more information, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="4079e-108">若要確保如果 WMI 發生失敗並重新啟動，managed 物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請在您的 MOF 檔案中使用 [**\# pragma 自動**](pragma-autorecover.md)復原語句預處理器指令。</span><span class="sxs-lookup"><span data-stu-id="4079e-108">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) statement preprocessor instruction in your MOF file.</span></span>

 

## <a name="base-class"></a><span data-ttu-id="4079e-109">基類</span><span class="sxs-lookup"><span data-stu-id="4079e-109">Base Class</span></span>

<span data-ttu-id="4079e-110">基類代表一些一般概念。</span><span class="sxs-lookup"><span data-stu-id="4079e-110">A base class represents some general concept.</span></span> <span data-ttu-id="4079e-111">例如， [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) 類別代表 WMI 中所有類型的 cd-rom 光碟機，並且包含描述所有 cd-rom 光碟機種類的一般屬性。</span><span class="sxs-lookup"><span data-stu-id="4079e-111">For example, the [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) class represents all types of CD-ROM drives in WMI, and contains general properties that describe all kinds of CD-ROM drives.</span></span> <span data-ttu-id="4079e-112">如需詳細資訊，請參閱 [建立基類（Base Class](creating-a-base-class.md)）。</span><span class="sxs-lookup"><span data-stu-id="4079e-112">For more information, see [Creating a Base Class](creating-a-base-class.md).</span></span>

<span data-ttu-id="4079e-113">衍生的類別會繼承其他類別的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="4079e-113">A derived class inherits properties and methods from another class.</span></span> <span data-ttu-id="4079e-114">衍生類別通常代表基類的特定案例。</span><span class="sxs-lookup"><span data-stu-id="4079e-114">A derived class usually represents a specific case of a base class.</span></span> <span data-ttu-id="4079e-115">例如， [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) 類別代表 Windows 系統上的 cd-rom 光碟機。</span><span class="sxs-lookup"><span data-stu-id="4079e-115">For example, the [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) class represents a CD-ROM drive on a Windows system.</span></span> <span data-ttu-id="4079e-116">**Win32 \_ CDROMDrive** 類別是以和繼承 [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive)的許多屬性為基礎。</span><span class="sxs-lookup"><span data-stu-id="4079e-116">The **Win32\_CDROMDrive** class is based on and inherits many of properties from [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span></span> <span data-ttu-id="4079e-117">不過， **Win32 \_ CDROMDrive** 和其他衍生類別一樣，可以有讓衍生類別成為唯一的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="4079e-117">However, **Win32\_CDROMDrive**, like other derived classes, can have additional properties that make the derived class unique.</span></span> <span data-ttu-id="4079e-118">如需詳細資訊，請參閱 [建立衍生類別](creating-a-derived-class.md)。</span><span class="sxs-lookup"><span data-stu-id="4079e-118">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

## <a name="properties-and-methods"></a><span data-ttu-id="4079e-119">屬性和方法</span><span class="sxs-lookup"><span data-stu-id="4079e-119">Properties and Methods</span></span>

<span data-ttu-id="4079e-120">建立類別表示定義描述該類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="4079e-120">Creating a class means defining the properties that describe that class.</span></span> <span data-ttu-id="4079e-121">您也可以定義方法，以操作類別所代表的物件。</span><span class="sxs-lookup"><span data-stu-id="4079e-121">You can also define methods that manipulate the object represented by the class.</span></span>

<span data-ttu-id="4079e-122">一般來說，屬性代表物件的某個層面，例如裝置的序號或進程的位元組大小，而方法則代表會變更裝置或邏輯實體之狀態或行為的動作。</span><span class="sxs-lookup"><span data-stu-id="4079e-122">Generally, a property represents an aspect of the object, such as a serial number for a device or a size in bytes for a process, while a method represents an action that changes the state or behavior of the device or logical entity.</span></span>

<span data-ttu-id="4079e-123">每個類別都至少必須有一個索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4079e-123">Each class must have at least one key property.</span></span> <span data-ttu-id="4079e-124">雖然類別可以有多個索引鍵，但您無法使用256個以上的索引鍵來建立類別的實例。</span><span class="sxs-lookup"><span data-stu-id="4079e-124">While a class may have multiple keys, you cannot create an instance of a class with more than 256 keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4079e-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="4079e-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4079e-126">設計受控物件格式 (MOF) 類別</span><span class="sxs-lookup"><span data-stu-id="4079e-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
