---
description: 設定或抓取要封裝之訊息的純文字內容。 這是預設屬性。
ms.assetid: 7927321f-fbda-45e0-9b9f-c10ecd3a98b1
title: EnvelopedData 內容屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ce87dba503d8e8eec2dc21a9024c1071b3255f3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976070"
---
# <a name="envelopeddatacontent-property"></a><span data-ttu-id="43870-104">EnvelopedData 內容屬性</span><span class="sxs-lookup"><span data-stu-id="43870-104">EnvelopedData.Content property</span></span>

<span data-ttu-id="43870-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="43870-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="43870-106">相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="43870-106">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="43870-107">**Content** 屬性會設定或抓取要封裝之訊息的純文字內容。</span><span class="sxs-lookup"><span data-stu-id="43870-107">The **Content** property sets or retrieves the plaintext content of a message to be enveloped.</span></span> <span data-ttu-id="43870-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="43870-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="43870-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="43870-109">Syntax</span></span>


```VB
EnvelopedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="43870-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="43870-110">Property value</span></span>

<span data-ttu-id="43870-111">要封裝之訊息的純文字內容。</span><span class="sxs-lookup"><span data-stu-id="43870-111">The plaintext content of a message to be enveloped.</span></span>

## <a name="remarks"></a><span data-ttu-id="43870-112">備註</span><span class="sxs-lookup"><span data-stu-id="43870-112">Remarks</span></span>

<span data-ttu-id="43870-113">設定此屬性必須在呼叫 [**加密**](envelopeddata-encrypt.md) 方法之前完成。</span><span class="sxs-lookup"><span data-stu-id="43870-113">Setting this property must be done before the [**Encrypt**](envelopeddata-encrypt.md) method is called.</span></span> <span data-ttu-id="43870-114">當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且會遺失物件中任何加密的內容。</span><span class="sxs-lookup"><span data-stu-id="43870-114">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset, and any encrypted content in the object is lost.</span></span>

## <a name="requirements"></a><span data-ttu-id="43870-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="43870-115">Requirements</span></span>



| <span data-ttu-id="43870-116">需求</span><span class="sxs-lookup"><span data-stu-id="43870-116">Requirement</span></span> | <span data-ttu-id="43870-117">值</span><span class="sxs-lookup"><span data-stu-id="43870-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43870-118">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="43870-118">End of client support</span></span><br/> | <span data-ttu-id="43870-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43870-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="43870-120">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="43870-120">End of server support</span></span><br/> | <span data-ttu-id="43870-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43870-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="43870-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="43870-122">Redistributable</span></span><br/>       | <span data-ttu-id="43870-123">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="43870-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="43870-124">DLL</span><span class="sxs-lookup"><span data-stu-id="43870-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="43870-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43870-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43870-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43870-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43870-127">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="43870-127">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
