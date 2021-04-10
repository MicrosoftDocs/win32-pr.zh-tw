---
description: CIM \_ 裝載類別代表檔案系統與其附加目錄之間的關聯。
ms.assetid: abf1833b-9b39-45c0-8400-2be2bf3a1c3c
ms.tgt_platform: multiple
title: CIM_Mount 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Mount
- CIM_Mount.Dependent
- CIM_Mount.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b86587466517a10302b3109a521e902a66892c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110964"
---
# <a name="cim_mount-class"></a><span data-ttu-id="323e7-103">CIM \_ 掛接類別</span><span class="sxs-lookup"><span data-stu-id="323e7-103">CIM\_Mount class</span></span>

<span data-ttu-id="323e7-104">**CIM \_ 裝載** 類別代表檔案系統與其附加目錄之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="323e7-104">The **CIM\_Mount** class represents an association between a file system and a directory to which it is attached.</span></span>

<span data-ttu-id="323e7-105">此關聯性的語義需要檔案系統 (透過檔案儲存關聯) 包含掛接的目錄，而該檔案與參考為相依的檔案系統不同。</span><span class="sxs-lookup"><span data-stu-id="323e7-105">The semantics of this relationship require that the mounted directory be contained by a file system (via the file storage association) that is different from the file system referenced as the dependent.</span></span> <span data-ttu-id="323e7-106">目錄的包含檔案系統可以是本機或遠端。</span><span class="sxs-lookup"><span data-stu-id="323e7-106">The directory's containing file system can be local or remote.</span></span> <span data-ttu-id="323e7-107">例如，Solaris 電腦系統上的本機檔案系統可從檔案系統掛接目錄（透過電腦的光碟機存取） (也就是另一個本機檔案系統) 。</span><span class="sxs-lookup"><span data-stu-id="323e7-107">For example, a local file system on a Solaris computer system can mount a directory from the file system accessed via the computer's CDROM drive (that is, another local file system).</span></span> <span data-ttu-id="323e7-108">另一方面，在「遠端」的情況下，它的檔案系統會先匯出目錄，而該目錄是裝載于另一部電腦系統，例如做為檔案伺服器。</span><span class="sxs-lookup"><span data-stu-id="323e7-108">On the other hand, in a "remote" case, the directory is first exported by its file system, which is hosted on another computer system acting, for example, as a file server.</span></span> <span data-ttu-id="323e7-109">若要區分這兩個裝載，應一律針對遠端存取/掛接的目錄定義 [**CIM \_ 匯出**](cim-export.md) 關聯。</span><span class="sxs-lookup"><span data-stu-id="323e7-109">To distinguish the two mounts, a [**CIM\_Export**](cim-export.md) association should always be defined for the remotely accessed/mounted directories.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="323e7-110">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="323e7-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="323e7-111">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="323e7-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="323e7-112">下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="323e7-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="323e7-113">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="323e7-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="323e7-114">語法</span><span class="sxs-lookup"><span data-stu-id="323e7-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{75BCF4F6-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Mount : CIM_Dependency
{
  CIM_NFS       REF Dependent;
  CIM_Directory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="323e7-115">成員</span><span class="sxs-lookup"><span data-stu-id="323e7-115">Members</span></span>

<span data-ttu-id="323e7-116">**CIM \_ 掛接** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="323e7-116">The **CIM\_Mount** class has these types of members:</span></span>

-   [<span data-ttu-id="323e7-117">屬性</span><span class="sxs-lookup"><span data-stu-id="323e7-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="323e7-118">屬性</span><span class="sxs-lookup"><span data-stu-id="323e7-118">Properties</span></span>

<span data-ttu-id="323e7-119">**CIM \_ 裝載** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="323e7-119">The **CIM\_Mount** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="323e7-120">**先行**</span><span class="sxs-lookup"><span data-stu-id="323e7-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="323e7-121">資料類型： **CIM \_ 目錄**</span><span class="sxs-lookup"><span data-stu-id="323e7-121">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="323e7-122">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="323e7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="323e7-123">限定詞： [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) ，覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) </span><span class="sxs-lookup"><span data-stu-id="323e7-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="323e7-124">描述裝載之目錄的 [**CIM \_ 目錄**](cim-directory.md) 。</span><span class="sxs-lookup"><span data-stu-id="323e7-124">A [**CIM\_Directory**](cim-directory.md) describing the directory mounted.</span></span>

</dd> <dt>

<span data-ttu-id="323e7-125">**依賴**</span><span class="sxs-lookup"><span data-stu-id="323e7-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="323e7-126">資料類型： **CIM \_ NFS**</span><span class="sxs-lookup"><span data-stu-id="323e7-126">Data type: **CIM\_NFS**</span></span>
</dt> <dt>

<span data-ttu-id="323e7-127">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="323e7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="323e7-128">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) </span><span class="sxs-lookup"><span data-stu-id="323e7-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="323e7-129">[**CIM \_ NFS**](cim-nfs.md) ，用來描述裝載目錄的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="323e7-129">A [**CIM\_NFS**](cim-nfs.md) describing the FileSystem the Directory is mounted on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="323e7-130">備註</span><span class="sxs-lookup"><span data-stu-id="323e7-130">Remarks</span></span>

<span data-ttu-id="323e7-131">**CIM \_掛接** 衍生自 [**CIM 相依 \_**](cim-dependency.md)性。</span><span class="sxs-lookup"><span data-stu-id="323e7-131">**CIM\_Mount** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="323e7-132">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="323e7-132">WMI does not implement this class.</span></span>

<span data-ttu-id="323e7-133">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="323e7-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="323e7-134">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="323e7-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="323e7-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="323e7-135">Requirements</span></span>



| <span data-ttu-id="323e7-136">需求</span><span class="sxs-lookup"><span data-stu-id="323e7-136">Requirement</span></span> | <span data-ttu-id="323e7-137">值</span><span class="sxs-lookup"><span data-stu-id="323e7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="323e7-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="323e7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="323e7-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="323e7-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="323e7-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="323e7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="323e7-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="323e7-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="323e7-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="323e7-142">Namespace</span></span><br/>                | <span data-ttu-id="323e7-143">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="323e7-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="323e7-144">MOF</span><span class="sxs-lookup"><span data-stu-id="323e7-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="323e7-145"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="323e7-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="323e7-146">DLL</span><span class="sxs-lookup"><span data-stu-id="323e7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="323e7-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="323e7-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="323e7-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="323e7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="323e7-149">**CIM \_ 相依性**</span><span class="sxs-lookup"><span data-stu-id="323e7-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

