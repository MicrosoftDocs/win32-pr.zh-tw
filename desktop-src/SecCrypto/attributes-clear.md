---
description: 清除集合中的所有屬性物件。
ms.assetid: 98b022f8-15aa-44b4-aaff-de09081d80b6
title: Attributes。 Clear 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eec570200234f455467c30a3eb12429226400c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995377"
---
# <a name="attributesclear-method"></a><span data-ttu-id="10b00-103">Attributes。 Clear 方法</span><span class="sxs-lookup"><span data-stu-id="10b00-103">Attributes.Clear method</span></span>

<span data-ttu-id="10b00-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="10b00-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="10b00-105">請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="10b00-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="10b00-106">**Clear** 方法會清除集合中的所有 [**屬性**](attribute.md)物件。</span><span class="sxs-lookup"><span data-stu-id="10b00-106">The **Clear** method clears all [**Attribute**](attribute.md) objects from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="10b00-107">語法</span><span class="sxs-lookup"><span data-stu-id="10b00-107">Syntax</span></span>


```VB
Attributes.Clear()
```



## <a name="parameters"></a><span data-ttu-id="10b00-108">參數</span><span class="sxs-lookup"><span data-stu-id="10b00-108">Parameters</span></span>

<span data-ttu-id="10b00-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="10b00-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="10b00-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="10b00-110">Return value</span></span>

<span data-ttu-id="10b00-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="10b00-111">This method does not return a value.</span></span> <span data-ttu-id="10b00-112">使用這個方法的應用程式必須包含程式碼，以處理此方法所引發的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="10b00-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b00-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="10b00-113">Requirements</span></span>



| <span data-ttu-id="10b00-114">需求</span><span class="sxs-lookup"><span data-stu-id="10b00-114">Requirement</span></span> | <span data-ttu-id="10b00-115">值</span><span class="sxs-lookup"><span data-stu-id="10b00-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="10b00-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="10b00-116">End of client support</span></span><br/> | <span data-ttu-id="10b00-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10b00-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="10b00-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="10b00-118">End of server support</span></span><br/> | <span data-ttu-id="10b00-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10b00-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="10b00-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="10b00-120">Redistributable</span></span><br/>       | <span data-ttu-id="10b00-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="10b00-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="10b00-122">DLL</span><span class="sxs-lookup"><span data-stu-id="10b00-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="10b00-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10b00-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10b00-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10b00-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10b00-125">加密物件</span><span class="sxs-lookup"><span data-stu-id="10b00-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="10b00-126">**屬性**</span><span class="sxs-lookup"><span data-stu-id="10b00-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
