---
description: Mergemod.dll 會呼叫 ConfigureModule 物件的 ProvideIntegerData 方法，以從用戶端工具中取出整數資料。
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: 'ConfigureModule. ProvideIntegerData 方法 (Mergemod .h) '
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
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981399"
---
# <a name="configuremoduleprovideintegerdata-method"></a><span data-ttu-id="5a8d7-103">ConfigureModule. ProvideIntegerData 方法</span><span class="sxs-lookup"><span data-stu-id="5a8d7-103">ConfigureModule.ProvideIntegerData method</span></span>

<span data-ttu-id="5a8d7-104">Mergemod.dll 會呼叫 [**ConfigureModule 物件**](configuremodule-object.md)的 **ProvideIntegerData** 方法，以從用戶端工具中取出整數資料。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-104">The **ProvideIntegerData** method of the [**ConfigureModule object**](configuremodule-object.md) is called by Mergemod.dll to retrieve integer data from the client tool.</span></span>

<span data-ttu-id="5a8d7-105">Mergemod.dll 從 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的對應專案提供 *名稱*。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-105">Mergemod.dll provides the *Name* from the corresponding entry in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="5a8d7-106">此工具應該會傳回 \_ [確定]，並在 *ConfigData* 中提供適當的自訂整數。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-106">The tool should return S\_OK and provide the appropriate customization integer in *ConfigData*.</span></span>

<span data-ttu-id="5a8d7-107">如果工具未提供任何此 *名稱* 值的設定資料，此函式應該會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-107">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="5a8d7-108">在此情況下 Mergemod.dll 會忽略 *ConfigData* 引數的值，並使用 ModuleConfiguration 資料表中的預設值。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-108">In this case Mergemod.dll ignores the value of the *ConfigData* argument and uses the Default value from the ModuleConfiguration table.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a8d7-109">語法</span><span class="sxs-lookup"><span data-stu-id="5a8d7-109">Syntax</span></span>


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="5a8d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="5a8d7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a8d7-111">*名稱*</span><span class="sxs-lookup"><span data-stu-id="5a8d7-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="5a8d7-112">要抓取資料的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-112">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="5a8d7-113">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="5a8d7-113">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="5a8d7-114">自訂文字的指標。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-114">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a8d7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a8d7-115">Return value</span></span>

<span data-ttu-id="5a8d7-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a8d7-117">備註</span><span class="sxs-lookup"><span data-stu-id="5a8d7-117">Remarks</span></span>

<span data-ttu-id="5a8d7-118">針對 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中的每一筆記錄，用戶端可能只會被呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-118">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="5a8d7-119">請注意，Mergemod.dll 永遠不會對相同的「名稱」值進行多個用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-119">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="5a8d7-120">如果 ModuleSubstitution 資料表中沒有任何記錄使用屬性，ModuleConfiguration 資料表中的專案就不會呼叫用戶端。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-120">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="5a8d7-121">C++</span><span class="sxs-lookup"><span data-stu-id="5a8d7-121">C++</span></span>

<span data-ttu-id="5a8d7-122">請參閱 [**ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata)函式。</span><span class="sxs-lookup"><span data-stu-id="5a8d7-122">See [**ProvideIntegerData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a8d7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a8d7-123">Requirements</span></span>



| <span data-ttu-id="5a8d7-124">需求</span><span class="sxs-lookup"><span data-stu-id="5a8d7-124">Requirement</span></span> | <span data-ttu-id="5a8d7-125">值</span><span class="sxs-lookup"><span data-stu-id="5a8d7-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8d7-126">版本</span><span class="sxs-lookup"><span data-stu-id="5a8d7-126">Version</span></span><br/> | <span data-ttu-id="5a8d7-127">Mergemod.dll 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5a8d7-127">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="5a8d7-128">標頭</span><span class="sxs-lookup"><span data-stu-id="5a8d7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5a8d7-129"><dt>Mergemod。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a8d7-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a8d7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5a8d7-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="5a8d7-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a8d7-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




