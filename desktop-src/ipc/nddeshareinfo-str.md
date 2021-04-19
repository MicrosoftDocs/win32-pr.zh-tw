---
description: 包含 NetDDE 共用資料庫管理員所維護的 DDE 共用屬性 (DSDM) 。
ms.assetid: f4101553-06ef-4f83-87c7-5b6fdf0467e5
title: 'NDDESHAREINFO 結構 (Nddeapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDDESHAREINFO
api_type:
- HeaderDef
api_location:
- Nddeapi.h
ms.openlocfilehash: 975382272a4e2c7cc56b0ddf593905b4d745a48b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980008"
---
# <a name="nddeshareinfo-structure"></a><span data-ttu-id="df440-103">NDDESHAREINFO 結構</span><span class="sxs-lookup"><span data-stu-id="df440-103">NDDESHAREINFO structure</span></span>

<span data-ttu-id="df440-104">\[不再支援網路 DDE。</span><span class="sxs-lookup"><span data-stu-id="df440-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="df440-105">Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]</span><span class="sxs-lookup"><span data-stu-id="df440-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="df440-106">包含 NetDDE 共用資料庫管理員所維護的 DDE 共用屬性 (DSDM) 。</span><span class="sxs-lookup"><span data-stu-id="df440-106">Contains DDE share attributes maintained by the NetDDE Share Database Manager (DSDM).</span></span> <span data-ttu-id="df440-107">與每個 DDE 共用相關聯的安全描述項不會透過此結構傳遞，但可透過特定的函式來存取。</span><span class="sxs-lookup"><span data-stu-id="df440-107">The security descriptor associated with each DDE share is not passed through this structure but is accessed through specific functions.</span></span> <span data-ttu-id="df440-108">NetDDE DSDM API 接受此結構來設定函數;針對取得函式，DSDM 會傳回封裝到所提供緩衝區中的結構，以及成員 **lpszShareName**、 **lpszAppTopicList** 和 **lpszItemList** 所參考的資料。</span><span class="sxs-lookup"><span data-stu-id="df440-108">The NetDDE DSDM API accepts this structure for set functions; for get functions, the DSDM returns the structure packed into the supplied buffer along with the data referenced by the members **lpszShareName**, **lpszAppTopicList**, and **lpszItemList**.</span></span>

## <a name="syntax"></a><span data-ttu-id="df440-109">語法</span><span class="sxs-lookup"><span data-stu-id="df440-109">Syntax</span></span>


```C++
typedef struct _NDDESHAREINFO {
  LONG   lRevision;
  LPTSTR lpszShareName;
  LONG   lShareType;
  LPTSTR lpszAppTopicList;
  LONG   fSharedFlag;
  LONG   fService;
  LONG   fStartAppFlag;
  LONG   nCmdShow;
  LONG   qModifyId[2];
  LONG   cNumItems;
  LPTSTR lpszItemList;
} NDDESHAREINFO, *PNDDESHAREINFO;
```



## <a name="members"></a><span data-ttu-id="df440-110">成員</span><span class="sxs-lookup"><span data-stu-id="df440-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="df440-111">**lRevision**</span><span class="sxs-lookup"><span data-stu-id="df440-111">**lRevision**</span></span>
</dt> <dd>

<span data-ttu-id="df440-112">**NDDESHAREINFO** 結構的修訂層級。</span><span class="sxs-lookup"><span data-stu-id="df440-112">The revision level of the **NDDESHAREINFO** structure.</span></span> <span data-ttu-id="df440-113">目前修訂層級為1。</span><span class="sxs-lookup"><span data-stu-id="df440-113">Currently, the revision level is 1.</span></span>

</dd> <dt>

<span data-ttu-id="df440-114">**lpszShareName**</span><span class="sxs-lookup"><span data-stu-id="df440-114">**lpszShareName**</span></span>
</dt> <dd>

<span data-ttu-id="df440-115">共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="df440-115">The name of the share.</span></span> <span data-ttu-id="df440-116">這個字串 \_ 的長度不得超過 NDDESHARENAME 字元數上限。</span><span class="sxs-lookup"><span data-stu-id="df440-116">This string must be no more than MAX\_NDDESHARENAME characters long.</span></span>

</dd> <dt>

<span data-ttu-id="df440-117">**lShareType**</span><span class="sxs-lookup"><span data-stu-id="df440-117">**lShareType**</span></span>
</dt> <dd>

<span data-ttu-id="df440-118">一或多個 DDE 共用類型。</span><span class="sxs-lookup"><span data-stu-id="df440-118">One or more DDE share types.</span></span> <span data-ttu-id="df440-119">這個成員可以是下列受支援之 DDE 共用類型的組合。</span><span class="sxs-lookup"><span data-stu-id="df440-119">This member can be a combination of the following supported DDE share types.</span></span>



| <span data-ttu-id="df440-120">共用類型</span><span class="sxs-lookup"><span data-stu-id="df440-120">Share type</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="df440-121">意義</span><span class="sxs-lookup"><span data-stu-id="df440-121">Meaning</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SHARE_TYPE_NEW"></span><span id="share_type_new"></span><dl> <span data-ttu-id="df440-122"><dt>**共用 \_輸入 \_ 新**</dt>的 <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="df440-122"><dt>**SHARE\_TYPE\_NEW**</dt> <dt>0x02</dt></span></span> </dl>          | <span data-ttu-id="df440-123">此共用包含 OLE 應用程式/主題配對。</span><span class="sxs-lookup"><span data-stu-id="df440-123">The share contains an OLE application/topic pair.</span></span><br/>   |
| <span id="SHARE_TYPE_OLD"></span><span id="share_type_old"></span><dl> <span data-ttu-id="df440-124"><dt>**共用 \_輸入 \_ 舊**</dt>的 <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="df440-124"><dt>**SHARE\_TYPE\_OLD**</dt> <dt>0x01</dt></span></span> </dl>          | <span data-ttu-id="df440-125">此共用包含一個 DDE 應用程式/主題配對。</span><span class="sxs-lookup"><span data-stu-id="df440-125">The share contains a DDE application/topic pair.</span></span><br/>    |
| <span id="SHARE_TYPE_STATIC"></span><span id="share_type_static"></span><dl> <span data-ttu-id="df440-126"><dt>**共用 \_輸入 \_ 靜態**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="df440-126"><dt>**SHARE\_TYPE\_STATIC**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="df440-127">共用包含靜態應用程式/主題組。</span><span class="sxs-lookup"><span data-stu-id="df440-127">The share contains a static application/topic pair.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="df440-128">**lpszAppTopicList**</span><span class="sxs-lookup"><span data-stu-id="df440-128">**lpszAppTopicList**</span></span>
</dt> <dd>

<span data-ttu-id="df440-129">緩衝區的指標，其中包含 DDE、OLE 和靜態應用程式/主題配對之以 null 結束的字串。</span><span class="sxs-lookup"><span data-stu-id="df440-129">A pointer to a buffer containing null-terminated strings for the DDE, OLE, and static application/topic pairs.</span></span> <span data-ttu-id="df440-130">緩衝區應該採用下列格式：</span><span class="sxs-lookup"><span data-stu-id="df440-130">The buffer should be in the following format:</span></span>

``` syntax
<DDE application name>|<DDE topic name>\0
<OLE application name>|<OLE topic name>\0
<static application name>|<static topic name>\0\0
```

</dd> <dt>

<span data-ttu-id="df440-131">**fSharedFlag**</span><span class="sxs-lookup"><span data-stu-id="df440-131">**fSharedFlag**</span></span>
</dt> <dd>

<span data-ttu-id="df440-132">如果這個成員是 **FALSE**，則 dde 共用將不允許遠端使用者透過使用 DDE 來進行通訊。</span><span class="sxs-lookup"><span data-stu-id="df440-132">If this member is **FALSE**, the DDE share will not allow remote users to communicate through it by using DDE.</span></span> <span data-ttu-id="df440-133">不過，本機使用者仍可透過 DDE 共用進行通訊。</span><span class="sxs-lookup"><span data-stu-id="df440-133">However, local users can still communicate through the DDE share.</span></span> <span data-ttu-id="df440-134">如果相關聯的 DACL 授與存取權，則一律隱含本機用戶端連結。</span><span class="sxs-lookup"><span data-stu-id="df440-134">Local client links are always implied if the associated DACL grants access.</span></span>

</dd> <dt>

<span data-ttu-id="df440-135">**fService**</span><span class="sxs-lookup"><span data-stu-id="df440-135">**fService**</span></span>
</dt> <dd>

<span data-ttu-id="df440-136">如果設定此成員，則在允許 DDE 通訊之前，DDE 共用將不會檢查目前的使用者是否已將其設定為受信任。</span><span class="sxs-lookup"><span data-stu-id="df440-136">If this member is set, the DDE share will not check whether the current user has set it as trusted before allowing DDE communication.</span></span>

</dd> <dt>

<span data-ttu-id="df440-137">**fStartAppFlag**</span><span class="sxs-lookup"><span data-stu-id="df440-137">**fStartAppFlag**</span></span>
</dt> <dd>

<span data-ttu-id="df440-138">如果已設定此成員，且共用受信任而無法啟動應用程式，則 NetDDE 會嘗試啟動 **lpszAppTopicList** 所指定的應用程式（如果它一開始無法與應用程式進行 DDE 交談）。</span><span class="sxs-lookup"><span data-stu-id="df440-138">If this member is set and the share is trusted to start applications, NetDDE will attempt to start the application specified by **lpszAppTopicList** if it cannot initially start a DDE conversation with the application.</span></span>

</dd> <dt>

<span data-ttu-id="df440-139">**nCmdShow**</span><span class="sxs-lookup"><span data-stu-id="df440-139">**nCmdShow**</span></span>
</dt> <dd>

<span data-ttu-id="df440-140">當 NetDDE 啟動應用程式以起始 DDE 交談時，會透過 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain)函式的 *nCmdShow* 參數，將此值傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="df440-140">When NetDDE starts an application to initiate a DDE conversation, this value is sent to the application through the *nCmdShow* parameter of the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="df440-141">它會定義要在其中顯示應用程式視窗的慣用模式。</span><span class="sxs-lookup"><span data-stu-id="df440-141">It defines the preferred mode for the application window to be shown in.</span></span> <span data-ttu-id="df440-142">只有在 **fStartAppFlag** 為作用中時，此參數才有意義。</span><span class="sxs-lookup"><span data-stu-id="df440-142">This parameter is significant only if **fStartAppFlag** is active.</span></span> <span data-ttu-id="df440-143">在應用程式啟動時，登入的使用者也可以在將共用升級為受信任狀態時，覆寫此選項。</span><span class="sxs-lookup"><span data-stu-id="df440-143">The logged on user in whose context the application is started can also override this option when promoting the share to trusted status.</span></span> <span data-ttu-id="df440-144">此成員的預設值為 SW \_ SHOWMAXIMIZED。</span><span class="sxs-lookup"><span data-stu-id="df440-144">The default for this member is SW\_SHOWMAXIMIZED.</span></span>

</dd> <dt>

<span data-ttu-id="df440-145">**qModifyId**</span><span class="sxs-lookup"><span data-stu-id="df440-145">**qModifyId**</span></span>
</dt> <dd>

<span data-ttu-id="df440-146">8位元組的序號，表示 DDE 共用的修改序號。</span><span class="sxs-lookup"><span data-stu-id="df440-146">An 8-byte serial number that indicates the modification serial number of the DDE share.</span></span> <span data-ttu-id="df440-147">每當 [**NDdeShareSetInfo**](nddesharesetinfo.md) 或 [**NDdeSetShareSecurity**](nddesetsharesecurity.md) 呼叫修改了 DDE 共用時，就會變更這些值。</span><span class="sxs-lookup"><span data-stu-id="df440-147">Every time the DDE share is modified by a [**NDdeShareSetInfo**](nddesharesetinfo.md) or [**NDdeSetShareSecurity**](nddesetsharesecurity.md) call, these values are changed.</span></span>

</dd> <dt>

<span data-ttu-id="df440-148">**cNumItems**</span><span class="sxs-lookup"><span data-stu-id="df440-148">**cNumItems**</span></span>
</dt> <dd>

<span data-ttu-id="df440-149">**LpszItemList** 中列出的專案數。</span><span class="sxs-lookup"><span data-stu-id="df440-149">The number of items listed in **lpszItemList**.</span></span> <span data-ttu-id="df440-150">如果 **cNumItems** 為零，則 **lpszItemList** 是空的，而且共用資訊和相關聯的安全描述項會套用至相關聯應用程式所服務的所有專案。</span><span class="sxs-lookup"><span data-stu-id="df440-150">If **cNumItems** is zero, then **lpszItemList** is empty, and the share information and associated security descriptor apply to all items serviced by the associated application.</span></span>

</dd> <dt>

<span data-ttu-id="df440-151">**lpszItemList**</span><span class="sxs-lookup"><span data-stu-id="df440-151">**lpszItemList**</span></span>
</dt> <dd>

<span data-ttu-id="df440-152">緩衝區的指標，其中包含以 null 終止的字串，可指定 DDE 交易中的用戶端應用程式可以要求或啟動建議迴圈的專案。</span><span class="sxs-lookup"><span data-stu-id="df440-152">A pointer to a buffer containing null-terminated strings that specify the items the client application in a DDE transaction can request or start advise loops on.</span></span> <span data-ttu-id="df440-153">如果未列出任何專案，則 DDE 共用允許使用任何專案。</span><span class="sxs-lookup"><span data-stu-id="df440-153">If no items are listed, the DDE share allows any item to be used.</span></span> <span data-ttu-id="df440-154">清單中的專案數必須符合 **cNumItems** 計數。</span><span class="sxs-lookup"><span data-stu-id="df440-154">The number of items in the list must match the **cNumItems** count.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df440-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="df440-155">Requirements</span></span>



| <span data-ttu-id="df440-156">需求</span><span class="sxs-lookup"><span data-stu-id="df440-156">Requirement</span></span> | <span data-ttu-id="df440-157">值</span><span class="sxs-lookup"><span data-stu-id="df440-157">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df440-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df440-158">Minimum supported client</span></span><br/> | <span data-ttu-id="df440-159">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df440-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="df440-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df440-160">Minimum supported server</span></span><br/> | <span data-ttu-id="df440-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df440-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="df440-162">標頭</span><span class="sxs-lookup"><span data-stu-id="df440-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="df440-163"><dt>Nddeapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="df440-163"><dt>Nddeapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df440-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df440-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df440-165">網路動態資料交換總覽</span><span class="sxs-lookup"><span data-stu-id="df440-165">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="df440-166">網路 DDE 結構</span><span class="sxs-lookup"><span data-stu-id="df440-166">Network DDE Structures</span></span>](network-dde-structures.md)
</dt> <dt>

[<span data-ttu-id="df440-167">**NDdeSetShareSecurity**</span><span class="sxs-lookup"><span data-stu-id="df440-167">**NDdeSetShareSecurity**</span></span>](nddesetsharesecurity.md)
</dt> <dt>

[<span data-ttu-id="df440-168">**NDdeShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="df440-168">**NDdeShareSetInfo**</span></span>](nddesharesetinfo.md)
</dt> <dt>

[<span data-ttu-id="df440-169">**WinMain**</span><span class="sxs-lookup"><span data-stu-id="df440-169">**WinMain**</span></span>](/windows/win32/api/winbase/nf-winbase-winmain)
</dt> </dl>

 

