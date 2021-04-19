---
description: 設定或抓取要簽署的資料。 這是預設屬性。
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: SignedData 內容屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998680"
---
# <a name="signeddatacontent-property"></a><span data-ttu-id="76dad-104">SignedData 內容屬性</span><span class="sxs-lookup"><span data-stu-id="76dad-104">SignedData.Content property</span></span>

<span data-ttu-id="76dad-105">\[[ **內容** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="76dad-105">\[The **Content** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="76dad-106">相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="76dad-106">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="76dad-107">**Content** 屬性會設定或抓取要簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="76dad-107">The **Content** property sets or retrieves the data to be signed.</span></span> <span data-ttu-id="76dad-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="76dad-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="76dad-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="76dad-109">Syntax</span></span>


```VB
SignedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="76dad-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="76dad-110">Property value</span></span>

<span data-ttu-id="76dad-111">要簽署的資料。</span><span class="sxs-lookup"><span data-stu-id="76dad-111">The data to be signed.</span></span>

## <a name="remarks"></a><span data-ttu-id="76dad-112">備註</span><span class="sxs-lookup"><span data-stu-id="76dad-112">Remarks</span></span>

<span data-ttu-id="76dad-113">這個屬性必須在呼叫 [**Sign**](signeddata-sign.md) 方法之前初始化。</span><span class="sxs-lookup"><span data-stu-id="76dad-113">This property must be initialized before the [**Sign**](signeddata-sign.md) method is called.</span></span> <span data-ttu-id="76dad-114">當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且在變更屬性之前與物件相關聯的任何簽章都會遺失。</span><span class="sxs-lookup"><span data-stu-id="76dad-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any signature that was associated with the object before the property was changed is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="76dad-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="76dad-115">Requirements</span></span>



| <span data-ttu-id="76dad-116">需求</span><span class="sxs-lookup"><span data-stu-id="76dad-116">Requirement</span></span> | <span data-ttu-id="76dad-117">值</span><span class="sxs-lookup"><span data-stu-id="76dad-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76dad-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="76dad-118">Redistributable</span></span><br/> | <span data-ttu-id="76dad-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="76dad-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="76dad-120">DLL</span><span class="sxs-lookup"><span data-stu-id="76dad-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="76dad-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76dad-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76dad-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76dad-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76dad-123">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="76dad-123">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
