---
title: 使用 Active Directory 服務介面的優點
description: ADSI 為系統管理員提供許多優點，如下表所述。
ms.assetid: 7afb1b70-635e-4527-bb53-dc9692ae4ebc
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，使用 ADSI 的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff20036146d1c35fde0d53e3748f21a82b87a8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020810"
---
# <a name="benefits-of-using-active-directory-service-interfaces"></a><span data-ttu-id="0fd72-104">使用 Active Directory 服務介面的優點</span><span class="sxs-lookup"><span data-stu-id="0fd72-104">Benefits of Using Active Directory Service Interfaces</span></span>

<span data-ttu-id="0fd72-105">ADSI 為系統管理員提供許多優點，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="0fd72-105">ADSI offers many benefits to system administrators, as described in the following table.</span></span>



| <span data-ttu-id="0fd72-106">功能</span><span class="sxs-lookup"><span data-stu-id="0fd72-106">Feature</span></span>                   | <span data-ttu-id="0fd72-107">優點</span><span class="sxs-lookup"><span data-stu-id="0fd72-107">Benefit</span></span>                                                                                                                                                                                                                                                                                                                             |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd72-108">開啟</span><span class="sxs-lookup"><span data-stu-id="0fd72-108">Open</span></span>                      | <span data-ttu-id="0fd72-109">任何目錄提供者都可以執行 ADSI 提供者;使用者可自由選擇目錄服務，而不會犧牲管理能力。</span><span class="sxs-lookup"><span data-stu-id="0fd72-109">Any directory provider can implement an ADSI provider; users gain freedom of choice in directory services without sacrificing manageability.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="0fd72-110">獨立于 DS</span><span class="sxs-lookup"><span data-stu-id="0fd72-110">DS independent</span></span>            | <span data-ttu-id="0fd72-111">系統管理應用程式未緊密系結至指定廠商的目錄服務。</span><span class="sxs-lookup"><span data-stu-id="0fd72-111">Administrative applications are not tightly bound to a given vendor's directory service.</span></span> <span data-ttu-id="0fd72-112">系統管理和其他已啟用目錄的應用程式可供開發，不需要瞭解廠商特定的目錄 Api。</span><span class="sxs-lookup"><span data-stu-id="0fd72-112">Administrative and other directory-enabled applications can be developed with no need to understand vendor-specific directory APIs.</span></span> <span data-ttu-id="0fd72-113">相同的應用程式可以在多個目錄上運作。</span><span class="sxs-lookup"><span data-stu-id="0fd72-113">The same application can work on multiple directories.</span></span> <span data-ttu-id="0fd72-114">縮短開發時間和支援成本。</span><span class="sxs-lookup"><span data-stu-id="0fd72-114">Development time and support costs are reduced.</span></span> |
| <span data-ttu-id="0fd72-115">多種語言支援</span><span class="sxs-lookup"><span data-stu-id="0fd72-115">Multiple language support</span></span> | <span data-ttu-id="0fd72-116">ADSI 物件透過元件物件模型，讓您輕鬆存取目錄服務。</span><span class="sxs-lookup"><span data-stu-id="0fd72-116">ADSI objects provide easy access to directory services through the component object model.</span></span> <span data-ttu-id="0fd72-117">COM 應用程式可以 Microsoft Visual Basic、Microsoft Visual Basic Scripting Edition (VBScript) 和 C/c + + 等語言撰寫。</span><span class="sxs-lookup"><span data-stu-id="0fd72-117">COM applications can be written in languages such as Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition (VBScript), and C/C++.</span></span>                                                                                             |
| <span data-ttu-id="0fd72-118">簡單的程式設計模型</span><span class="sxs-lookup"><span data-stu-id="0fd72-118">Simple programming model</span></span>  | <span data-ttu-id="0fd72-119">ADSI 是由一組小型、易於學習的介面所組成。</span><span class="sxs-lookup"><span data-stu-id="0fd72-119">ADSI consists of a small, easy-to-learn set of interfaces.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="0fd72-120">可編寫腳本</span><span class="sxs-lookup"><span data-stu-id="0fd72-120">Scriptable</span></span>                | <span data-ttu-id="0fd72-121">任何 Automation 相容語言 (例如 Visual Basic、VBScript、Perl、Rexx 和其他) 都可用來開發目錄服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="0fd72-121">Any Automation compatible language (for example, Visual Basic, VBScript, Perl, Rexx, and others) can be used to develop directory service applications.</span></span> <span data-ttu-id="0fd72-122">系統管理員和開發人員可以使用熟悉的工具。</span><span class="sxs-lookup"><span data-stu-id="0fd72-122">Administrators and developers can use the tools they already know.</span></span> <span data-ttu-id="0fd72-123">提高產能，降低開發時間和支援成本。</span><span class="sxs-lookup"><span data-stu-id="0fd72-123">Productivity is enhanced — development time and support costs are reduced.</span></span>                               |
| <span data-ttu-id="0fd72-124">功能豐富</span><span class="sxs-lookup"><span data-stu-id="0fd72-124">Functionally rich</span></span>         | <span data-ttu-id="0fd72-125">Isv 和精密的使用者可以使用用於簡單編寫腳本之系統管理應用程式的相同 ADSI 模型來開發嚴重的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0fd72-125">ISVs and sophisticated end users can develop serious applications using the same ADSI models that are used for simple scripted administrative applications.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="0fd72-126">可延伸</span><span class="sxs-lookup"><span data-stu-id="0fd72-126">Extensible</span></span>                | <span data-ttu-id="0fd72-127">目錄提供者、Isv 和使用者可以利用新的物件和函式來擴充 ADSI，以增加價值或符合獨特需求。</span><span class="sxs-lookup"><span data-stu-id="0fd72-127">Directory providers, ISVs, and end users can extend ADSI with new objects and functions to add value or meet unique needs.</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="0fd72-128">OLE DB 感知</span><span class="sxs-lookup"><span data-stu-id="0fd72-128">OLE DB aware</span></span>              | <span data-ttu-id="0fd72-129">ADSI 提供 OLE DB 介面，讓熟悉資料庫程式設計的程式 OLE DB 設計人員可以快速提升生產力。</span><span class="sxs-lookup"><span data-stu-id="0fd72-129">ADSI provides an OLE DB interface so that programmers familiar with database programming through OLE DB can be productive quickly.</span></span>                                                                                                                                                                                                  |



 

 

 




