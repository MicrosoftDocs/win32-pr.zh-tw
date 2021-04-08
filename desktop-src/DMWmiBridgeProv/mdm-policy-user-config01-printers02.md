---
title: MDM_Policy_User_Config01_Printers02 類別
description: MDM \_ Policy \_ User \_ Config01 \_ Printers02 類別代表可用的印表機原則。
ms.assetid: 9faeaa04-92b4-43b0-be17-0f85f2eb493c
keywords:
- MDM_Policy_User_Config01_Printers02 類別
- MDM_Policy_User_Config01_Printers02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Printers02
- MDM_Policy_User_Config01_Printers02.InstanceID
- MDM_Policy_User_Config01_Printers02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04be571473f05d93242c77d02052cf84c335caf4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685947"
---
# <a name="mdm_policy_user_config01_printers02-class"></a><span data-ttu-id="1d9ce-105">MDM \_ 原則 \_ 使用者 \_ Config01 \_ Printers02 類別</span><span class="sxs-lookup"><span data-stu-id="1d9ce-105">MDM\_Policy\_User\_Config01\_Printers02 class</span></span>

<span data-ttu-id="1d9ce-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="1d9ce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1d9ce-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="1d9ce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1d9ce-108">MDM \_ Policy \_ User \_ Config01 \_ Printers02 類別代表可用的印表機原則。</span><span class="sxs-lookup"><span data-stu-id="1d9ce-108">The MDM\_Policy\_User\_Config01\_Printers02 class represents the available printer policies.</span></span>

<span data-ttu-id="1d9ce-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d9ce-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9ce-110">語法</span><span class="sxs-lookup"><span data-stu-id="1d9ce-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Printers02
{
  string InstanceID;
  string ParentID;
  string PointAndPrintRestrictions_User;
};
```

## <a name="members"></a><span data-ttu-id="1d9ce-111">成員</span><span class="sxs-lookup"><span data-stu-id="1d9ce-111">Members</span></span>

<span data-ttu-id="1d9ce-112">**MDM \_ Policy \_ User \_ Config01 \_ Printers02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1d9ce-112">The **MDM\_Policy\_User\_Config01\_Printers02** class has these types of members:</span></span>

-   [<span data-ttu-id="1d9ce-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1d9ce-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1d9ce-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1d9ce-114">Properties</span></span>

<span data-ttu-id="1d9ce-115">**MDM \_ Policy \_ User \_ Config01 \_ Printers02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1d9ce-115">The **MDM\_Policy\_User\_Config01\_Printers02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d9ce-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1d9ce-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9ce-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1d9ce-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9ce-118">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d9ce-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9ce-119">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d9ce-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1d9ce-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1d9ce-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9ce-121">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1d9ce-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9ce-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1d9ce-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d9ce-123">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1d9ce-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1d9ce-124">PointAndPrintRestrictions \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="1d9ce-124">PointAndPrintRestrictions\_User</span></span>](/windows/client-management/mdm/policy-csp-printers#printers-pointandprintrestrictions-user)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d9ce-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1d9ce-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d9ce-126">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1d9ce-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d9ce-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d9ce-127">Requirements</span></span>



| <span data-ttu-id="1d9ce-128">需求</span><span class="sxs-lookup"><span data-stu-id="1d9ce-128">Requirement</span></span> | <span data-ttu-id="1d9ce-129">值</span><span class="sxs-lookup"><span data-stu-id="1d9ce-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9ce-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d9ce-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1d9ce-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d9ce-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d9ce-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d9ce-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1d9ce-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="1d9ce-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1d9ce-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d9ce-134">Namespace</span></span><br/>                | <span data-ttu-id="1d9ce-135">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="1d9ce-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1d9ce-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1d9ce-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d9ce-137"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d9ce-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d9ce-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1d9ce-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d9ce-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d9ce-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

