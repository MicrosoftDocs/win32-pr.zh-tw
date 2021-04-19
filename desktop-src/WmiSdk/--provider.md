---
description: 作為 \_ \_ Win32Provider 系統類別的父類別。
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: __Provider 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977955"
---
# <a name="__provider-class"></a><span data-ttu-id="6eea7-103">\_\_提供者類別</span><span class="sxs-lookup"><span data-stu-id="6eea7-103">\_\_Provider class</span></span>

<span data-ttu-id="6eea7-104">**\_ \_ Provider** system 類別是抽象基類，可做為 [**\_ \_ Win32Provider**](--win32provider.md)系統類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="6eea7-104">The **\_\_Provider** system class is an abstract base class that serves as the parent class for the [**\_\_Win32Provider**](--win32provider.md) system class.</span></span>

<span data-ttu-id="6eea7-105">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="6eea7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6eea7-106">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="6eea7-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eea7-107">語法</span><span class="sxs-lookup"><span data-stu-id="6eea7-107">Syntax</span></span>

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="6eea7-108">成員</span><span class="sxs-lookup"><span data-stu-id="6eea7-108">Members</span></span>

<span data-ttu-id="6eea7-109">**\_ \_ 提供者** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6eea7-109">The **\_\_Provider** class has these types of members:</span></span>

-   [<span data-ttu-id="6eea7-110">屬性</span><span class="sxs-lookup"><span data-stu-id="6eea7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6eea7-111">屬性</span><span class="sxs-lookup"><span data-stu-id="6eea7-111">Properties</span></span>

<span data-ttu-id="6eea7-112">**\_ \_ 提供者** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="6eea7-112">The **\_\_Provider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6eea7-113">**名稱**</span><span class="sxs-lookup"><span data-stu-id="6eea7-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6eea7-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6eea7-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6eea7-115">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="6eea7-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="6eea7-116">限定詞：索引 [**鍵**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6eea7-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6eea7-117">可唯一識別提供者的語言中性字元串。</span><span class="sxs-lookup"><span data-stu-id="6eea7-117">Language-neutral string that uniquely identifies the provider.</span></span> <span data-ttu-id="6eea7-118">建議採用下列格式來防止命名衝突：</span><span class="sxs-lookup"><span data-stu-id="6eea7-118">The following format is suggested to prevent naming conflicts:</span></span>

<span data-ttu-id="6eea7-119">廠商 \| 提供者 \| 版本</span><span class="sxs-lookup"><span data-stu-id="6eea7-119">vendor\|provider\|version</span></span>

<span data-ttu-id="6eea7-120">例如，此提供者名稱代表 Microsoft TestProvider 的1.0 版：</span><span class="sxs-lookup"><span data-stu-id="6eea7-120">For example, this provider name represents version 1.0 of the Microsoft TestProvider:</span></span>

<span data-ttu-id="6eea7-121">"Microsoft \| TestProvider v1.0 \| "</span><span class="sxs-lookup"><span data-stu-id="6eea7-121">"Microsoft\|TestProvider\|V1.0"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6eea7-122">備註</span><span class="sxs-lookup"><span data-stu-id="6eea7-122">Remarks</span></span>

<span data-ttu-id="6eea7-123">**\_ \_ 提供者** 類別衍生自沒有屬性的 [**\_ \_ SystemClass**](--systemclass.md)。</span><span class="sxs-lookup"><span data-stu-id="6eea7-123">The **\_\_Provider** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="6eea7-124">提供者會建立 [**\_ \_ Win32Provider**](--win32provider.md)實例，以指定其實體執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6eea7-124">Providers create [**\_\_Win32Provider**](--win32provider.md) instances to specify information about their physical implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eea7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="6eea7-125">Requirements</span></span>



| <span data-ttu-id="6eea7-126">需求</span><span class="sxs-lookup"><span data-stu-id="6eea7-126">Requirement</span></span> | <span data-ttu-id="6eea7-127">值</span><span class="sxs-lookup"><span data-stu-id="6eea7-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6eea7-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6eea7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6eea7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6eea7-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6eea7-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6eea7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6eea7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6eea7-131">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6eea7-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="6eea7-132">Namespace</span></span><br/>                | <span data-ttu-id="6eea7-133">所有 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="6eea7-133">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6eea7-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6eea7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eea7-135">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="6eea7-135">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="6eea7-136">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="6eea7-136">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6eea7-137">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="6eea7-137">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

