---
description: 受保護的儲存體可為應用程式提供一個介面，以儲存必須保持安全或無需修改的使用者資料。
ms.assetid: 85c1a009-c4f7-4b5a-ad96-6845a4e80de9
title: PStore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d291b911c351cce10827b7937c6a474b7c570
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972538"
---
# <a name="pstore"></a><span data-ttu-id="9008d-103">PStore</span><span class="sxs-lookup"><span data-stu-id="9008d-103">PStore</span></span>

<span data-ttu-id="9008d-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="9008d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="9008d-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="9008d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="9008d-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="9008d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="9008d-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="9008d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="9008d-108">受保護的儲存體可為應用程式提供一個介面，以儲存必須保持安全或無需修改的使用者資料。</span><span class="sxs-lookup"><span data-stu-id="9008d-108">Protected Storage provides applications with an interface to store user data that must be kept secure or free from modification.</span></span>

<span data-ttu-id="9008d-109">儲存的資料單位稱為「專案」。</span><span class="sxs-lookup"><span data-stu-id="9008d-109">Units of data stored are called Items.</span></span> <span data-ttu-id="9008d-110">所儲存資料的結構和內容對受保護的儲存系統而言是不透明的。</span><span class="sxs-lookup"><span data-stu-id="9008d-110">The structure and content of the stored data is opaque to the Protected Storage system.</span></span> <span data-ttu-id="9008d-111">存取專案時，可能會根據使用者定義的安全性樣式進行確認，這會指定存取資料所需的確認，例如是否需要密碼。</span><span class="sxs-lookup"><span data-stu-id="9008d-111">Access to Items is subject to confirmation according to a user-defined Security Style, which specifies what confirmation is required to access the data, such as whether a password is required.</span></span> <span data-ttu-id="9008d-112">此外，對專案的存取會受到存取規則集的規範。</span><span class="sxs-lookup"><span data-stu-id="9008d-112">In addition, access to Items is subject to an Access rule set.</span></span> <span data-ttu-id="9008d-113">每個存取模式都有存取規則：例如，讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="9008d-113">There is an Access rule for each Access Mode: for example, read/write.</span></span> <span data-ttu-id="9008d-114">存取規則集是由存取子句所組成。</span><span class="sxs-lookup"><span data-stu-id="9008d-114">Access rule sets are composed of Access Clauses.</span></span> <span data-ttu-id="9008d-115">目前支援兩種存取子句：呼叫端的 Authenticode 和二元檢查。</span><span class="sxs-lookup"><span data-stu-id="9008d-115">Two kinds of Access Clauses are currently supported: Authenticode and Binary Check of caller.</span></span> <span data-ttu-id="9008d-116">通常在應用程式設定時，會提供一種機制，讓新的應用程式向使用者要求可能已由其他應用程式建立的專案存取權。</span><span class="sxs-lookup"><span data-stu-id="9008d-116">Typically at application setup time, a mechanism is provided to allow a new application to request from the user access to Items that may have been created previously by another application.</span></span>

<span data-ttu-id="9008d-117">專案是由索引鍵、類型、子類型和名稱的組合來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="9008d-117">Items are uniquely identified by the combination of a Key, Type, Subtype, and Name.</span></span> <span data-ttu-id="9008d-118">索引鍵是一個常數，可指定專案是否為此電腦的全域專案，或僅與此使用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="9008d-118">The Key is a constant that specifies whether the Item is global to this computer or associated only with this user.</span></span> <span data-ttu-id="9008d-119">名稱是一個字串，通常是由使用者選擇。</span><span class="sxs-lookup"><span data-stu-id="9008d-119">The Name is a string, generally chosen by the user.</span></span> <span data-ttu-id="9008d-120">類型和子類型為 **GUID** s，通常是由應用程式指定。</span><span class="sxs-lookup"><span data-stu-id="9008d-120">Type and Subtype are **GUID** s, generally specified by the application.</span></span> <span data-ttu-id="9008d-121">類型和子類型的其他資訊會保存在系統登錄中，並包含顯示名稱和 UI 提示等屬性。</span><span class="sxs-lookup"><span data-stu-id="9008d-121">Additional information about Types and Subtypes is kept in the system registry and include attributes such as Display Name and UI hints.</span></span> <span data-ttu-id="9008d-122">子類型的父類型是固定的，並且包含在系統登錄中做為屬性。</span><span class="sxs-lookup"><span data-stu-id="9008d-122">For Subtypes, the parent Type is fixed and included in the system registry as an attribute.</span></span> <span data-ttu-id="9008d-123">類型群組專案是用於一般用途：例如，付款或識別。</span><span class="sxs-lookup"><span data-stu-id="9008d-123">The Type group Items is used for a common purpose: for example, Payment or Identification.</span></span> <span data-ttu-id="9008d-124">子類型群組專案共用一般的資料格式。</span><span class="sxs-lookup"><span data-stu-id="9008d-124">The Subtype group Items share a common data format.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9008d-125">本節內容</span><span class="sxs-lookup"><span data-stu-id="9008d-125">In this section</span></span>

-   [<span data-ttu-id="9008d-126">**IEnumPStoreItems**</span><span class="sxs-lookup"><span data-stu-id="9008d-126">**IEnumPStoreItems**</span></span>](ienumpstoreitems.md)
-   [<span data-ttu-id="9008d-127">**IEnumPStoreProviders**</span><span class="sxs-lookup"><span data-stu-id="9008d-127">**IEnumPStoreProviders**</span></span>](ienumpstoreproviders.md)
-   [<span data-ttu-id="9008d-128">**IEnumPStoreTypes**</span><span class="sxs-lookup"><span data-stu-id="9008d-128">**IEnumPStoreTypes**</span></span>](ienumpstoretypes.md)
-   [<span data-ttu-id="9008d-129">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="9008d-129">**IPStore**</span></span>](ipstore.md)
-   [<span data-ttu-id="9008d-130">**PStoreCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="9008d-130">**PStoreCreateInstance**</span></span>](pstorecreateinstance.md)
-   [<span data-ttu-id="9008d-131">**PStoreEnumProviders**</span><span class="sxs-lookup"><span data-stu-id="9008d-131">**PStoreEnumProviders**</span></span>](pstoreenumproviders.md)
-   [<span data-ttu-id="9008d-132">**PStore 常數**</span><span class="sxs-lookup"><span data-stu-id="9008d-132">**PStore Constants**</span></span>](pstore-constants.md)
-   [<span data-ttu-id="9008d-133">**PStore 類型**</span><span class="sxs-lookup"><span data-stu-id="9008d-133">**PStore Types**</span></span>](pstore-types.md)

 

 
