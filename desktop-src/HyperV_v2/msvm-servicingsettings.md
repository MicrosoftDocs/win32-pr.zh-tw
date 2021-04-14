---
description: 包含在服務作業期間使用的設定。
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Msvm_ServicingSettings 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469221"
---
# <a name="msvm_servicingsettings-class"></a><span data-ttu-id="1f69b-103">Msvm \_ ServicingSettings 類別</span><span class="sxs-lookup"><span data-stu-id="1f69b-103">Msvm\_ServicingSettings class</span></span>

<span data-ttu-id="1f69b-104">包含在服務作業期間使用的設定。</span><span class="sxs-lookup"><span data-stu-id="1f69b-104">Contains settings used during servicing operations.</span></span>

<span data-ttu-id="1f69b-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1f69b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f69b-106">語法</span><span class="sxs-lookup"><span data-stu-id="1f69b-106">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="1f69b-107">成員</span><span class="sxs-lookup"><span data-stu-id="1f69b-107">Members</span></span>

<span data-ttu-id="1f69b-108">**Msvm \_ ServicingSettings** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1f69b-108">The **Msvm\_ServicingSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="1f69b-109">屬性</span><span class="sxs-lookup"><span data-stu-id="1f69b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1f69b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="1f69b-110">Properties</span></span>

<span data-ttu-id="1f69b-111">**Msvm \_ ServicingSettings** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1f69b-111">The **Msvm\_ServicingSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1f69b-112">**版本**</span><span class="sxs-lookup"><span data-stu-id="1f69b-112">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1f69b-113">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1f69b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1f69b-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1f69b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1f69b-115">包含類別定義的版本。</span><span class="sxs-lookup"><span data-stu-id="1f69b-115">Contains the class definition's version.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f69b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f69b-116">Requirements</span></span>



| <span data-ttu-id="1f69b-117">需求</span><span class="sxs-lookup"><span data-stu-id="1f69b-117">Requirement</span></span> | <span data-ttu-id="1f69b-118">值</span><span class="sxs-lookup"><span data-stu-id="1f69b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f69b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1f69b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1f69b-120">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f69b-120">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1f69b-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1f69b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1f69b-122">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1f69b-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f69b-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="1f69b-123">Namespace</span></span><br/>                | <span data-ttu-id="1f69b-124">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1f69b-124">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1f69b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="1f69b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1f69b-126"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1f69b-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1f69b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1f69b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f69b-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1f69b-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




