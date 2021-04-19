---
description: SetAlias 方法會為位址設定預設的 H. 323 別名。 此別名將用於 h.264 呼叫設定 exchange，讓另一方知道此合作物件的名稱。
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'IH323LineEx：： SetAlias 方法 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995925"
---
# <a name="ih323lineexsetalias-method"></a><span data-ttu-id="8ae73-104">IH323LineEx：： SetAlias 方法</span><span class="sxs-lookup"><span data-stu-id="8ae73-104">IH323LineEx::SetAlias method</span></span>

<span data-ttu-id="8ae73-105">\[**SetAlias** 無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="8ae73-105">\[**SetAlias** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8ae73-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="8ae73-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8ae73-107">**SetAlias** 方法會為位址設定預設的 H. 323 別名。</span><span class="sxs-lookup"><span data-stu-id="8ae73-107">The **SetAlias** method configures a default H.323 alias for the address.</span></span> <span data-ttu-id="8ae73-108">此別名將用於 h.264 呼叫設定 exchange，讓另一方知道此合作物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="8ae73-108">This alias will be used in the H.323 call setup exchange so that the other party knows the name of this party.</span></span>

<span data-ttu-id="8ae73-109">第二次呼叫這個方法將會覆寫前一個別名。</span><span class="sxs-lookup"><span data-stu-id="8ae73-109">Calling this method a second time will overwrite the previous alias.</span></span>

<span data-ttu-id="8ae73-110">只有當 TSP 沒有其他方法可尋找適當的別名時，才會使用此介面上設定的別名。</span><span class="sxs-lookup"><span data-stu-id="8ae73-110">The alias set on this interface will be used only when there is no other way for the TSP to find a proper alias.</span></span> <span data-ttu-id="8ae73-111">未來，將閘道管理員支援新增至 TSP 時，註冊至閘道管理員或由閘道管理員指派的別名將會覆寫透過這個方法所設定的任何內容。</span><span class="sxs-lookup"><span data-stu-id="8ae73-111">In the future, when gatekeeper support is added into the TSP, the alias registered to the gatekeeper or assigned by the gatekeeper will override whatever is set through this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae73-112">語法</span><span class="sxs-lookup"><span data-stu-id="8ae73-112">Syntax</span></span>


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="8ae73-113">參數</span><span class="sxs-lookup"><span data-stu-id="8ae73-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae73-114">*strAlias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ae73-114">*strAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae73-115">要使用的別名（以 Unicode 為依據）。</span><span class="sxs-lookup"><span data-stu-id="8ae73-115">The alias to be used, in Unicode.</span></span> <span data-ttu-id="8ae73-116">不需要 **Null** 終止。</span><span class="sxs-lookup"><span data-stu-id="8ae73-116">**Null** termination is not required.</span></span>

</dd> <dt>

<span data-ttu-id="8ae73-117">*dwLength* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ae73-117">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ae73-118">別名名稱的長度（以字元數為單位），包括 **null** 結束字元。</span><span class="sxs-lookup"><span data-stu-id="8ae73-118">The length of the alias name in number of characters, including the **null** terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae73-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ae73-119">Return value</span></span>

<span data-ttu-id="8ae73-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8ae73-120">This method can return one of these values.</span></span>



| <span data-ttu-id="8ae73-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8ae73-121">Return code</span></span>                                                                               | <span data-ttu-id="8ae73-122">Description</span><span class="sxs-lookup"><span data-stu-id="8ae73-122">Description</span></span>                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ae73-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae73-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8ae73-124">方法成功。</span><span class="sxs-lookup"><span data-stu-id="8ae73-124">Method succeeded.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="8ae73-125"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae73-125"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="8ae73-126">*DwLength* 中指出的字元數超過 *strAlias* 參數中的實際字元數。</span><span class="sxs-lookup"><span data-stu-id="8ae73-126">The number of characters indicated in *dwLength* exceeds the actual number of characters in the *strAlias* parameter.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ae73-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ae73-127">Requirements</span></span>



| <span data-ttu-id="8ae73-128">需求</span><span class="sxs-lookup"><span data-stu-id="8ae73-128">Requirement</span></span> | <span data-ttu-id="8ae73-129">值</span><span class="sxs-lookup"><span data-stu-id="8ae73-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae73-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="8ae73-130">TAPI version</span></span><br/> | <span data-ttu-id="8ae73-131">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8ae73-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8ae73-132">標頭</span><span class="sxs-lookup"><span data-stu-id="8ae73-132">Header</span></span><br/>       | <dl> <span data-ttu-id="8ae73-133"><dt>H323priv。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ae73-133"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="8ae73-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ae73-134">Library</span></span><br/>      | <dl> <span data-ttu-id="8ae73-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="8ae73-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8ae73-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8ae73-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="8ae73-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ae73-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




