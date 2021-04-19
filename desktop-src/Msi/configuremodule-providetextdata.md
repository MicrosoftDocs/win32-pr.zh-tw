---
description: Mergemod.dll 會呼叫 ProvideTextData 方法，以從用戶端工具取出文字資料。 Mergemod.dll 從 ModuleConfiguration 資料表中的對應專案提供名稱。
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: 'ConfigureModule. ProvideTextData 方法 (Mergemod .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978488"
---
# <a name="configuremoduleprovidetextdata-method"></a><span data-ttu-id="5a186-104">ConfigureModule. ProvideTextData 方法</span><span class="sxs-lookup"><span data-stu-id="5a186-104">ConfigureModule.ProvideTextData method</span></span>

<span data-ttu-id="5a186-105">Mergemod.dll 會呼叫 **ProvideTextData** 方法，以從用戶端工具取出文字資料。</span><span class="sxs-lookup"><span data-stu-id="5a186-105">The **ProvideTextData** method is called by Mergemod.dll to retrieve text data from the client tool.</span></span> <span data-ttu-id="5a186-106">Mergemod.dll 從 ModuleConfiguration 資料表中的對應專案提供 *名稱* 。</span><span class="sxs-lookup"><span data-stu-id="5a186-106">Mergemod.dll provides the *Name* from the corresponding entry in the ModuleConfiguration table.</span></span>

<span data-ttu-id="5a186-107">此工具應該會傳回 \_ [確定]，並在 ConfigData 中提供適當的自訂文字。</span><span class="sxs-lookup"><span data-stu-id="5a186-107">The tool should return S\_OK and provide the appropriate customization text in ConfigData.</span></span> <span data-ttu-id="5a186-108">用戶端工具負責配置資料，但 Mergemod.dll負責釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="5a186-108">The client tool is responsible for allocating the data, but Mergemod.dllis responsible for releasing the memory.</span></span> <span data-ttu-id="5a186-109">此引數必須是 **BSTR** 物件。</span><span class="sxs-lookup"><span data-stu-id="5a186-109">This argument MUST be a **BSTR** object.</span></span> <span data-ttu-id="5a186-110">不接受 **LPCWSTR** 。</span><span class="sxs-lookup"><span data-stu-id="5a186-110">**LPCWSTR** is NOT accepted.</span></span>

<span data-ttu-id="5a186-111">如果工具未提供任何此 *名稱* 值的設定資料，此函式應該會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="5a186-111">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="5a186-112">在此情況下 Mergemod.dll 會忽略 ConfigData 引數的值，並使用 ModuleConfiguration 資料表中的預設值。</span><span class="sxs-lookup"><span data-stu-id="5a186-112">In this case Mergemod.dll ignores the value of the ConfigData argument and uses the Default value from the ModuleConfiguration table.</span></span>

<span data-ttu-id="5a186-113">如果) 開啟記錄檔，則任何不是 S \_ OK 或 s FALSE 的傳回碼 \_ 都會導致記錄錯誤 (，並導致合併失敗。</span><span class="sxs-lookup"><span data-stu-id="5a186-113">Any return code other than S\_OK or S\_FALSE will cause an error to be logged (if a log is open) and will result in the merge failing.</span></span>

<span data-ttu-id="5a186-114">因為此函式遵循標準 **BSTR** 慣例，所以 null 相當於空字串。</span><span class="sxs-lookup"><span data-stu-id="5a186-114">Because this function follows standard **BSTR** convention, null is equivalent to the empty string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a186-115">語法</span><span class="sxs-lookup"><span data-stu-id="5a186-115">Syntax</span></span>


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="5a186-116">參數</span><span class="sxs-lookup"><span data-stu-id="5a186-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a186-117">*名稱*</span><span class="sxs-lookup"><span data-stu-id="5a186-117">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="5a186-118">要抓取資料的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="5a186-118">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="5a186-119">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="5a186-119">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="5a186-120">自訂文字的指標。</span><span class="sxs-lookup"><span data-stu-id="5a186-120">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a186-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a186-121">Return value</span></span>

<span data-ttu-id="5a186-122">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5a186-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a186-123">備註</span><span class="sxs-lookup"><span data-stu-id="5a186-123">Remarks</span></span>

<span data-ttu-id="5a186-124">針對 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的每一筆記錄，用戶端可能只會被呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="5a186-124">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="5a186-125">請注意，Mergemod.dll 永遠不會對相同的「名稱」值進行多個用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="5a186-125">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="5a186-126">如果 ModuleSubstitution 資料表中沒有任何記錄使用屬性，ModuleConfiguration 資料表中的專案就不會呼叫用戶端。</span><span class="sxs-lookup"><span data-stu-id="5a186-126">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="5a186-127">C++</span><span class="sxs-lookup"><span data-stu-id="5a186-127">C++</span></span>

<span data-ttu-id="5a186-128">請參閱 [**ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata)函式。</span><span class="sxs-lookup"><span data-stu-id="5a186-128">See [**ProvideTextData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a186-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a186-129">Requirements</span></span>



| <span data-ttu-id="5a186-130">需求</span><span class="sxs-lookup"><span data-stu-id="5a186-130">Requirement</span></span> | <span data-ttu-id="5a186-131">值</span><span class="sxs-lookup"><span data-stu-id="5a186-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a186-132">版本</span><span class="sxs-lookup"><span data-stu-id="5a186-132">Version</span></span><br/> | <span data-ttu-id="5a186-133">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5a186-133">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5a186-134">標頭</span><span class="sxs-lookup"><span data-stu-id="5a186-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5a186-135"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a186-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a186-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5a186-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a186-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a186-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




