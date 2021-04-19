---
description: 設定或抓取識別碼的 OID 點值。
ms.assetid: bb960e65-776e-4ae8-a557-62254dc10558
title: 老。Value 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d8c3c59cfd3eadfb8aec56c6814a2af6ce9ff900
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978516"
---
# <a name="oidvalue-property"></a><span data-ttu-id="f38b2-103">老。Value 屬性</span><span class="sxs-lookup"><span data-stu-id="f38b2-103">OID.Value property</span></span>

<span data-ttu-id="f38b2-104">\[[ **值** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f38b2-104">\[The **Value** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f38b2-105">相反地，請在 [**system.object**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true)命名空間中使用 [**Oid 類別**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="f38b2-105">Instead, use the [**Oid Class**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="f38b2-106">**Value** 屬性會設定或抓取識別碼的 OID 點值。</span><span class="sxs-lookup"><span data-stu-id="f38b2-106">The **Value** property sets or retrieves the value of the OID dotted number of the identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="f38b2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f38b2-107">Syntax</span></span>


```VB
OID.Value As String
```



## <a name="property-value"></a><span data-ttu-id="f38b2-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="f38b2-108">Property value</span></span>

<span data-ttu-id="f38b2-109">識別碼的 OID 點值。</span><span class="sxs-lookup"><span data-stu-id="f38b2-109">The value of the OID dotted number of the identifier.</span></span> <span data-ttu-id="f38b2-110">如需可能的值，請參閱 Wincrypt。</span><span class="sxs-lookup"><span data-stu-id="f38b2-110">For possible values, see Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="f38b2-111">備註</span><span class="sxs-lookup"><span data-stu-id="f38b2-111">Remarks</span></span>

<span data-ttu-id="f38b2-112">如果已設定 **Value** 屬性， [**FriendlyName**](oid-friendlyname.md) 屬性會設定為對應的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f38b2-112">If the **Value** property is set, the [**FriendlyName**](oid-friendlyname.md) property is set to the corresponding display name.</span></span> <span data-ttu-id="f38b2-113">如果已設定 [ **FriendlyName** ] 屬性，則 [ **值** ] 屬性會設定為對應的點值。</span><span class="sxs-lookup"><span data-stu-id="f38b2-113">If the **FriendlyName** property is set, the **Value** property is set to the corresponding dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f38b2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f38b2-114">Requirements</span></span>



| <span data-ttu-id="f38b2-115">需求</span><span class="sxs-lookup"><span data-stu-id="f38b2-115">Requirement</span></span> | <span data-ttu-id="f38b2-116">值</span><span class="sxs-lookup"><span data-stu-id="f38b2-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f38b2-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f38b2-117">Redistributable</span></span><br/> | <span data-ttu-id="f38b2-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f38b2-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f38b2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="f38b2-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="f38b2-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f38b2-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f38b2-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f38b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f38b2-122">**老**</span><span class="sxs-lookup"><span data-stu-id="f38b2-122">**OID**</span></span>](oid.md)
</dt> </dl>

 

 
