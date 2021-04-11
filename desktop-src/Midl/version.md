---
title: version 屬性
description: '\ Version \ 介面屬性會識別多個 RPC 介面版本之間的特定版本。 有了 version 屬性，您就可以確保只允許相容版本的用戶端和伺服器軟體進行系結。'
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- version 屬性 MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022500"
---
# <a name="version-attribute"></a><span data-ttu-id="248bb-105">version 屬性</span><span class="sxs-lookup"><span data-stu-id="248bb-105">version attribute</span></span>

<span data-ttu-id="248bb-106">**\[ Version \]** 介面屬性會識別多個 RPC 介面版本之間的特定版本。</span><span class="sxs-lookup"><span data-stu-id="248bb-106">The **\[version\]** interface attribute identifies a particular version among multiple versions of an RPC interface.</span></span> <span data-ttu-id="248bb-107">有了 version 屬性，您就可以確保只允許相容版本的用戶端和伺服器軟體進行系結。</span><span class="sxs-lookup"><span data-stu-id="248bb-107">With the version attribute, you ensure that only compatible versions of client and server software are allowed to bind.</span></span>

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a><span data-ttu-id="248bb-108">參數</span><span class="sxs-lookup"><span data-stu-id="248bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="248bb-109">*主要值*</span><span class="sxs-lookup"><span data-stu-id="248bb-109">*major-value*</span></span> 
</dt> <dd>

<span data-ttu-id="248bb-110">指定零到65535（含）之間的簡短不帶正負號的整數，代表主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="248bb-110">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="248bb-111">*次要值*</span><span class="sxs-lookup"><span data-stu-id="248bb-111">*minor-value*</span></span> 
</dt> <dd>

<span data-ttu-id="248bb-112">指定零到65535（含）之間的簡短不帶正負號的整數，表示次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="248bb-112">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the minor version number.</span></span> <span data-ttu-id="248bb-113">次要版本值是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="248bb-113">The minor version value is optional.</span></span> <span data-ttu-id="248bb-114">如果有的話，次要版本值會與主要版本號碼分開， ( 的句點字元。 ) 。</span><span class="sxs-lookup"><span data-stu-id="248bb-114">If present, the minor version value is separated from the major version number by a period character (.).</span></span> <span data-ttu-id="248bb-115">如果未指定，次要版本值為零。</span><span class="sxs-lookup"><span data-stu-id="248bb-115">If not specified, the minor version value is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="248bb-116">備註</span><span class="sxs-lookup"><span data-stu-id="248bb-116">Remarks</span></span>

<span data-ttu-id="248bb-117">MIDL 編譯器不支援多個版本的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="248bb-117">The MIDL compiler does not support multiple versions of a COM interface.</span></span> <span data-ttu-id="248bb-118">因此，包含物件屬性的介面屬性清單 **\[** [](object.md) **\]** 不能包含 **\[ \] version** 屬性。</span><span class="sxs-lookup"><span data-stu-id="248bb-118">As a result, an interface attribute list that includes the **\[**[**object**](object.md)**\]** attribute cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="248bb-119">若要建立現有 COM 介面的新版本，請使用介面繼承。</span><span class="sxs-lookup"><span data-stu-id="248bb-119">To create a new version of an existing COM interface, use interface inheritance.</span></span> <span data-ttu-id="248bb-120">衍生的 COM 介面具有不同的 UUID，但繼承了基底介面的介面成員函式、狀態碼和介面屬性。</span><span class="sxs-lookup"><span data-stu-id="248bb-120">A derived COM interface has a different UUID but inherits the interface member functions, status codes, and interface attributes of the base interface.</span></span>

<span data-ttu-id="248bb-121">**\[** [](uuid.md) **\]** **\[ 版本 \]** 值與 uuid 值組合，可唯一識別介面。</span><span class="sxs-lookup"><span data-stu-id="248bb-121">In combination with the **\[**[**uuid**](uuid.md)**\]** value, the **\[version\]** value uniquely identifies the interface.</span></span> <span data-ttu-id="248bb-122">當用戶端呼叫遠端函式時，執行時間程式庫會將 **\[ 版本 \]** 和 **\[ uuid \]** 值傳遞至伺服器。</span><span class="sxs-lookup"><span data-stu-id="248bb-122">The run-time library passes the **\[version\]** and **\[uuid\]** values to the server when the client calls a remote function.</span></span> <span data-ttu-id="248bb-123">如果有下列情況，用戶端可以系結至指定介面的伺服器：</span><span class="sxs-lookup"><span data-stu-id="248bb-123">A client can bind to a server for a given interface if:</span></span>

-   <span data-ttu-id="248bb-124">**\[ Uuid \]** 值相同。</span><span class="sxs-lookup"><span data-stu-id="248bb-124">The **\[uuid\]** value is the same.</span></span>
-   <span data-ttu-id="248bb-125">主要版本號碼相同。</span><span class="sxs-lookup"><span data-stu-id="248bb-125">The major version number is the same.</span></span>
-   <span data-ttu-id="248bb-126">用戶端的次要版本號碼小於或等於伺服器的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="248bb-126">The client's minor version number is less than or equal to the server's minor version number.</span></span>

<span data-ttu-id="248bb-127">這是您的權益和使用者在 versionsÂ之間保有最大相容性的優點，也就是修改介面，只變更次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="248bb-127">It is to your benefit and your users' benefit to retain upward compatibility among versionsÂ that is, to modify the interface so that only the minor version number changes.</span></span> <span data-ttu-id="248bb-128">當您加入的新資料類型不是現有的函式所使用的新資料類型，以及加入新函式而不變更現有函式的介面規格時，您可以保留最新的相容性。</span><span class="sxs-lookup"><span data-stu-id="248bb-128">You can retain upward compatibility when you add new data types that are not used by existing functions and when you add new functions without changing the interface specification for existing functions.</span></span>

<span data-ttu-id="248bb-129">如果有下列任何一種情況，請變更主要版本號碼：</span><span class="sxs-lookup"><span data-stu-id="248bb-129">Change the major version number if any one of the following conditions apply:</span></span>

-   <span data-ttu-id="248bb-130">如果您變更現有函數所使用的資料類型。</span><span class="sxs-lookup"><span data-stu-id="248bb-130">If you change a data type that is used by an existing function.</span></span>
-   <span data-ttu-id="248bb-131">如果您變更現有函數的介面規格 (例如新增或移除參數) 。</span><span class="sxs-lookup"><span data-stu-id="248bb-131">If you change the interface specification for an existing function (such as adding or removing a parameter).</span></span>
-   <span data-ttu-id="248bb-132">如果您加入現有函式所呼叫的回呼。</span><span class="sxs-lookup"><span data-stu-id="248bb-132">If you add callbacks that are called by existing functions.</span></span>

<span data-ttu-id="248bb-133">如果下列所有條件都適用，請變更次要版本號碼：</span><span class="sxs-lookup"><span data-stu-id="248bb-133">Change the minor version number if all of the following conditions apply:</span></span>

-   <span data-ttu-id="248bb-134">如果您加入的型別定義或常數未由任何現有的函數或回呼所使用。</span><span class="sxs-lookup"><span data-stu-id="248bb-134">If you add type definitions or constants that are not used by any existing functions or callbacks.</span></span>
-   <span data-ttu-id="248bb-135">如果您未變更任何現有的函式，並將新函式加入至介面。</span><span class="sxs-lookup"><span data-stu-id="248bb-135">If you do not change any existing functions and you add new functions to the interface.</span></span>
-   <span data-ttu-id="248bb-136">如果您加入的回呼未由任何現有的函式所呼叫，且新的回呼遵循任何現有的函數。</span><span class="sxs-lookup"><span data-stu-id="248bb-136">If you add callbacks that are not called by any existing functions and the new callbacks follow any existing functions.</span></span>

<span data-ttu-id="248bb-137">如果您的修改符合對介面的最高層相容性變更，請使用下列程式。</span><span class="sxs-lookup"><span data-stu-id="248bb-137">If your modifications qualify as an upward-compatible change to the interface, use the following procedure.</span></span>

<span data-ttu-id="248bb-138">**若要修改 (IDL) 檔案的介面**</span><span class="sxs-lookup"><span data-stu-id="248bb-138">**To modify the interface (IDL) file**</span></span>

1.  <span data-ttu-id="248bb-139">在介面檔中加入新的常數和類型定義。</span><span class="sxs-lookup"><span data-stu-id="248bb-139">Add new constant and type definitions to the interface file.</span></span>
2.  <span data-ttu-id="248bb-140">將回呼函式加入至介面檔案的結尾。</span><span class="sxs-lookup"><span data-stu-id="248bb-140">Add callback functions to the end of the interface file.</span></span>
3.  <span data-ttu-id="248bb-141">將新函式加入至介面檔案的結尾。</span><span class="sxs-lookup"><span data-stu-id="248bb-141">Add new functions to the end of the interface file.</span></span>

<span data-ttu-id="248bb-142">在介面標頭中最多隻能出現一次 **\[ version \]** 屬性。</span><span class="sxs-lookup"><span data-stu-id="248bb-142">The **\[version\]** attribute can occur at most once in the interface header.</span></span>

<span data-ttu-id="248bb-143">當 version 屬性不存在時，介面的預設版本為0.0。</span><span class="sxs-lookup"><span data-stu-id="248bb-143">When the version attribute is not present, the interface has a default version of 0.0.</span></span>

<span data-ttu-id="248bb-144">主要與次要數位之間的句號字元是分隔符號，不代表小數點。</span><span class="sxs-lookup"><span data-stu-id="248bb-144">The period character between the major and minor numbers is a delimiter and does not represent a decimal point.</span></span> <span data-ttu-id="248bb-145">次要號碼會被視為整數。</span><span class="sxs-lookup"><span data-stu-id="248bb-145">The minor number is treated as an integer.</span></span> <span data-ttu-id="248bb-146">前置零並不重要。</span><span class="sxs-lookup"><span data-stu-id="248bb-146">Leading zeroes are not significant.</span></span> <span data-ttu-id="248bb-147">尾端的零是很重要的。</span><span class="sxs-lookup"><span data-stu-id="248bb-147">Trailing zeroes are significant.</span></span>

<span data-ttu-id="248bb-148">例如，版本設定1.11 代表一個主要值，而一個小數值為11。</span><span class="sxs-lookup"><span data-stu-id="248bb-148">For example, the version setting 1.11 represents a major value of one and a minor value of eleven.</span></span> <span data-ttu-id="248bb-149">1.11 版不代表介於1.1 和1.2 之間的值。</span><span class="sxs-lookup"><span data-stu-id="248bb-149">Version 1.11 does not represent a value between 1.1 and 1.2.</span></span>

## <a name="see-also"></a><span data-ttu-id="248bb-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="248bb-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="248bb-151"> (IDL) 檔案的介面定義</span><span class="sxs-lookup"><span data-stu-id="248bb-151">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="248bb-152">**介面**</span><span class="sxs-lookup"><span data-stu-id="248bb-152">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="248bb-153">**物件**</span><span class="sxs-lookup"><span data-stu-id="248bb-153">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="248bb-154">**uuid**</span><span class="sxs-lookup"><span data-stu-id="248bb-154">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




