---
description: 將設定資料與 managed 元素產生關聯。
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: CIM_SettingsDefineState 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1931b365108bb7b3df4269ae6acbb78292a0401d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985232"
---
# <a name="cim_settingsdefinestate-class"></a><span data-ttu-id="1d9f9-103">CIM \_ SettingsDefineState 類別</span><span class="sxs-lookup"><span data-stu-id="1d9f9-103">CIM\_SettingsDefineState class</span></span>

<span data-ttu-id="1d9f9-104">將設定資料與 managed 元素產生關聯。</span><span class="sxs-lookup"><span data-stu-id="1d9f9-104">Associates settings data with a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9f9-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d9f9-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="1d9f9-106">成員</span><span class="sxs-lookup"><span data-stu-id="1d9f9-106">Members</span></span>

<span data-ttu-id="1d9f9-107">**CIM \_ SettingsDefineState** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1d9f9-107">The **CIM\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="1d9f9-108">屬性</span><span class="sxs-lookup"><span data-stu-id="1d9f9-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d9f9-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1d9f9-109">Properties</span></span>

<span data-ttu-id="1d9f9-110">**CIM \_ SettingsDefineState** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1d9f9-110">The **CIM\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d9f9-111">**ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="1d9f9-111">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9f9-112">資料類型： **CIM \_ ManagedElement**</span><span class="sxs-lookup"><span data-stu-id="1d9f9-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="1d9f9-113">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d9f9-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9f9-114">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d9f9-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1d9f9-115">關聯中的 managed 元素。</span><span class="sxs-lookup"><span data-stu-id="1d9f9-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="1d9f9-116">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="1d9f9-116">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9f9-117">資料類型： **CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="1d9f9-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="1d9f9-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d9f9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9f9-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d9f9-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1d9f9-120">關聯中的設定資料。</span><span class="sxs-lookup"><span data-stu-id="1d9f9-120">The settings data in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d9f9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d9f9-121">Requirements</span></span>



| <span data-ttu-id="1d9f9-122">需求</span><span class="sxs-lookup"><span data-stu-id="1d9f9-122">Requirement</span></span> | <span data-ttu-id="1d9f9-123">值</span><span class="sxs-lookup"><span data-stu-id="1d9f9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9f9-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d9f9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1d9f9-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1d9f9-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1d9f9-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d9f9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1d9f9-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1d9f9-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1d9f9-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d9f9-128">Namespace</span></span><br/>                | <span data-ttu-id="1d9f9-129">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="1d9f9-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1d9f9-130">MOF</span><span class="sxs-lookup"><span data-stu-id="1d9f9-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d9f9-131"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1d9f9-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d9f9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1d9f9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d9f9-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d9f9-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

