---
title: MSAD_ReplCursor 類別
description: 提供有關指定命名內容的所有複本 (NC) 的輸入複寫狀態資訊。
ms.assetid: 5746cfe9-b113-4be3-b609-15cb937c271b
ms.tgt_platform: multiple
keywords:
- MSAD_ReplCursor 類別 Active Directory
- MSAD_ReplCursor 類別 Active Directory，描述
topic_type:
- apiref
api_name:
- MSAD_ReplCursor
- MSAD_ReplCursor.NamingContextDN
- MSAD_ReplCursor.SourceDsaInvocationID
- MSAD_ReplCursor.USNAttributeFilter
- MSAD_ReplCursor.SourceDsaDN
- MSAD_ReplCursor.TimeOfLastSuccessfulSync
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725ac8e9eee9f921ce4109e0b0e42ed85e75ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465393"
---
# <a name="msad_replcursor-class"></a><span data-ttu-id="c8f9b-105">MSAD \_ ReplCursor 類別</span><span class="sxs-lookup"><span data-stu-id="c8f9b-105">MSAD\_ReplCursor class</span></span>

<span data-ttu-id="c8f9b-106">提供有關指定命名內容的所有複本 (NC) 的輸入複寫狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-106">Provides inbound replication state information about all replicas of a given naming context (NC).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f9b-107">語法</span><span class="sxs-lookup"><span data-stu-id="c8f9b-107">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplCursor
{
  String   NamingContextDN;
  String   SourceDsaInvocationID;
  uint64   USNAttributeFilter;
  String   SourceDsaDN;
  datetime TimeOfLastSuccessfulSync;
};
```

## <a name="members"></a><span data-ttu-id="c8f9b-108">成員</span><span class="sxs-lookup"><span data-stu-id="c8f9b-108">Members</span></span>

<span data-ttu-id="c8f9b-109">**MSAD \_ ReplCursor** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c8f9b-109">The **MSAD\_ReplCursor** class has these types of members:</span></span>

-   [<span data-ttu-id="c8f9b-110">屬性</span><span class="sxs-lookup"><span data-stu-id="c8f9b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8f9b-111">屬性</span><span class="sxs-lookup"><span data-stu-id="c8f9b-111">Properties</span></span>

<span data-ttu-id="c8f9b-112">**MSAD \_ ReplCursor** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-112">The **MSAD\_ReplCursor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8f9b-113">**NamingCoNtextDN**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-113">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8f9b-114">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-114">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c8f9b-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8f9b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8f9b-116">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c8f9b-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c8f9b-117">取得保存此資料指標的命名內容 (NC) 的 X. 500 路徑。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-117">Gets the X.500 path for the naming context (NC) that holds this cursor.</span></span>

</dd> <dt>

<span data-ttu-id="c8f9b-118">**SourceDsaDN**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-118">**SourceDsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8f9b-119">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-119">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c8f9b-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8f9b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8f9b-121">取得目錄服務代理程式 (DSA) 的 X. 500 路徑，該路徑代表 (DC) 的來源網域控制站。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-121">Gets the X.500 path for the directory system agent (DSA) that represents the source domain controller (DC).</span></span>

</dd> <dt>

<span data-ttu-id="c8f9b-122">**SourceDsaInvocationID**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-122">**SourceDsaInvocationID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8f9b-123">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-123">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="c8f9b-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8f9b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8f9b-125">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c8f9b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c8f9b-126">取得 **USNAttributeFilter** 所對應之源伺服器的調用識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-126">Gets the invocation identifier of the originating server to which the **USNAttributeFilter** corresponds.</span></span>

</dd> <dt>

<span data-ttu-id="c8f9b-127">**TimeOfLastSuccessfulSync**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-127">**TimeOfLastSuccessfulSync**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8f9b-128">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c8f9b-129">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8f9b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8f9b-130">取得上次與來源 DSA 成功複寫同步處理的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-130">Gets the timestamp of the last successful replication sync with the source DSA.</span></span> <span data-ttu-id="c8f9b-131">指出此 DC 上次看到此 NC 來源 DSA 上所做變更的時間。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-131">Indicates the time when this DC last saw changes made on the source DSA for this NC.</span></span>

</dd> <dt>

<span data-ttu-id="c8f9b-132">**USNAttributeFilter**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-132">**USNAttributeFilter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8f9b-133">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c8f9b-134">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="c8f9b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c8f9b-135">取得目的地伺服器在更新序號小於或等於此更新序號時，所產生之所有變更所產生的更新序號（最大值）。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-135">Gets the maximum update sequence number to which the destination server can indicate that it has recorded all changes originated by the given server at update sequence numbers less than, or equal to, this update sequence number.</span></span> <span data-ttu-id="c8f9b-136">這個屬性是用來篩選目的地伺服器已套用於複寫來源伺服器的變更。</span><span class="sxs-lookup"><span data-stu-id="c8f9b-136">This property is used to filter changes that the destination server has already applied at replication source servers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8f9b-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8f9b-137">Requirements</span></span>



| <span data-ttu-id="c8f9b-138">需求</span><span class="sxs-lookup"><span data-stu-id="c8f9b-138">Requirement</span></span> | <span data-ttu-id="c8f9b-139">值</span><span class="sxs-lookup"><span data-stu-id="c8f9b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f9b-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8f9b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f9b-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="c8f9b-141">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c8f9b-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8f9b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f9b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8f9b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c8f9b-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="c8f9b-144">Namespace</span></span><br/>                | <span data-ttu-id="c8f9b-145">根 \\ MicrosoftActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="c8f9b-145">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="c8f9b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="c8f9b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8f9b-147"><dt>Replprov.dll mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8f9b-147"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8f9b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c8f9b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8f9b-149"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8f9b-149"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f9b-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8f9b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f9b-151">**DS 複寫資料 \_ \_ 指標**</span><span class="sxs-lookup"><span data-stu-id="c8f9b-151">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
</dt> </dl>

 

