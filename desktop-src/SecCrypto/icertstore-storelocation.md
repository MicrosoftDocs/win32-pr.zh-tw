---
description: 設定或抓取 \_ 憑證存放區的 CAPICOM 存放區 \_ 位置。
ms.assetid: 2bb76f51-f092-4dbe-93e9-1fdc185c7c50
title: ICertStore：： StoreLocation 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreLocation
- ICertStore.get_StoreLocation
- ICertStore.put_StoreLocation
- CertStore.StoreLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 97bca7ed9dae20c129d202910b40f7c26d54a576
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997767"
---
# <a name="icertstorestorelocation-property"></a><span data-ttu-id="c31f5-103">ICertStore：： StoreLocation 屬性</span><span class="sxs-lookup"><span data-stu-id="c31f5-103">ICertStore::StoreLocation property</span></span>

<span data-ttu-id="c31f5-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。\]</span><span class="sxs-lookup"><span data-stu-id="c31f5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="c31f5-105">**StoreLocation** 屬性會設定或抓取證書存儲的 [**CAPICOM \_ 存放區 \_ 位置**](capicom-store-location.md)。</span><span class="sxs-lookup"><span data-stu-id="c31f5-105">The **StoreLocation** property sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span>

<span data-ttu-id="c31f5-106">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c31f5-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c31f5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c31f5-107">Syntax</span></span>


```VB
CertStore.StoreLocation As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="c31f5-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="c31f5-108">Property value</span></span>

<span data-ttu-id="c31f5-109">憑證存放區的位置。</span><span class="sxs-lookup"><span data-stu-id="c31f5-109">The location of the certificate store.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c31f5-110">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c31f5-110">Error codes</span></span>

<span data-ttu-id="c31f5-111">如果屬性存取方法 **put \_ StoreLocation** 並 **讓 \_ StoreLocation** 成功，則會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c31f5-111">If the property access methods **put\_StoreLocation** and **get\_StoreLocation** succeed, they return S\_OK.</span></span>

<span data-ttu-id="c31f5-112">任何其他 **HRESULT** 值都表示呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="c31f5-112">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c31f5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="c31f5-113">Requirements</span></span>



| <span data-ttu-id="c31f5-114">需求</span><span class="sxs-lookup"><span data-stu-id="c31f5-114">Requirement</span></span> | <span data-ttu-id="c31f5-115">值</span><span class="sxs-lookup"><span data-stu-id="c31f5-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c31f5-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c31f5-116">Redistributable</span></span><br/> | <span data-ttu-id="c31f5-117">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c31f5-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c31f5-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c31f5-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="c31f5-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c31f5-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c31f5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c31f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c31f5-121">**ICertStore**</span><span class="sxs-lookup"><span data-stu-id="c31f5-121">**ICertStore**</span></span>](icertstore.md)
</dt> </dl>

 

 




