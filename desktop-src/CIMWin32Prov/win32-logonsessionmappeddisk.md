---
description: Win32 \_ LogonSessionMappedDisk 類別代表登入會話與會話內所定義之對應邏輯磁片之間的關聯。
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Win32_LogonSessionMappedDisk 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510728"
---
# <a name="win32_logonsessionmappeddisk-class"></a><span data-ttu-id="42ee1-103">Win32 \_ LogonSessionMappedDisk 類別</span><span class="sxs-lookup"><span data-stu-id="42ee1-103">Win32\_LogonSessionMappedDisk class</span></span>

<span data-ttu-id="42ee1-104">Win32 \_ LogonSessionMappedDisk 類別代表登入會話與會話內所定義之對應邏輯磁片之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="42ee1-104">The Win32\_LogonSessionMappedDisk class represents an association between a logon session and the mapped logical disks defined within the session.</span></span>

<span data-ttu-id="42ee1-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="42ee1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ee1-106">語法</span><span class="sxs-lookup"><span data-stu-id="42ee1-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="42ee1-107">成員</span><span class="sxs-lookup"><span data-stu-id="42ee1-107">Members</span></span>

<span data-ttu-id="42ee1-108">**Win32 \_ LogonSessionMappedDisk** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42ee1-108">The **Win32\_LogonSessionMappedDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="42ee1-109">屬性</span><span class="sxs-lookup"><span data-stu-id="42ee1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42ee1-110">屬性</span><span class="sxs-lookup"><span data-stu-id="42ee1-110">Properties</span></span>

<span data-ttu-id="42ee1-111">**Win32 \_ LogonSessionMappedDisk** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="42ee1-111">The **Win32\_LogonSessionMappedDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42ee1-112">**先行**</span><span class="sxs-lookup"><span data-stu-id="42ee1-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ee1-113">資料類型： **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="42ee1-113">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="42ee1-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42ee1-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42ee1-115">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42ee1-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42ee1-116">前面的屬性會參考登入會話。</span><span class="sxs-lookup"><span data-stu-id="42ee1-116">The Antecedent property references a logon session.</span></span>

</dd> <dt>

<span data-ttu-id="42ee1-117">**依賴**</span><span class="sxs-lookup"><span data-stu-id="42ee1-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ee1-118">資料類型： **Win32 \_ MappedLogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="42ee1-118">Data type: **Win32\_MappedLogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="42ee1-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="42ee1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42ee1-120">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ，索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="42ee1-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="42ee1-121">相依屬性會參考在 Antecedent 屬性所參考的會話內所定義的對應邏輯磁片。</span><span class="sxs-lookup"><span data-stu-id="42ee1-121">The Dependent property references a mapped logical disk defined within the session referenced by the Antecedent property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42ee1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="42ee1-122">Requirements</span></span>



| <span data-ttu-id="42ee1-123">需求</span><span class="sxs-lookup"><span data-stu-id="42ee1-123">Requirement</span></span> | <span data-ttu-id="42ee1-124">值</span><span class="sxs-lookup"><span data-stu-id="42ee1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42ee1-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42ee1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="42ee1-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42ee1-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42ee1-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42ee1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="42ee1-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42ee1-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42ee1-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="42ee1-129">Namespace</span></span><br/>                | <span data-ttu-id="42ee1-130">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="42ee1-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="42ee1-131">MOF</span><span class="sxs-lookup"><span data-stu-id="42ee1-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42ee1-132"><dt>CimWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="42ee1-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="42ee1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="42ee1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42ee1-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42ee1-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ee1-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42ee1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ee1-136">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="42ee1-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

