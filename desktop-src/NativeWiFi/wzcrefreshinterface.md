---
description: 重新整理特定無線區域網路介面的介面資訊。
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: 'WZCRefreshInterface 函式 (Wzcsapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 3f2ac1bd546403dca781b3a132b44f96d80bb5c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320220"
---
# <a name="wzcrefreshinterface-function"></a><span data-ttu-id="99b17-103">WZCRefreshInterface 函式</span><span class="sxs-lookup"><span data-stu-id="99b17-103">WZCRefreshInterface function</span></span>

<span data-ttu-id="99b17-104">\[在 Windows Vista 和 Windows Server 2008 中，不支援 **WZCRefreshInterface** 。</span><span class="sxs-lookup"><span data-stu-id="99b17-104">\[**WZCRefreshInterface** is not supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="99b17-105">相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。</span><span class="sxs-lookup"><span data-stu-id="99b17-105">Instead, use the [Native Wifi API](native-wifi-reference.md), which provides similar functionality.</span></span> <span data-ttu-id="99b17-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]</span><span class="sxs-lookup"><span data-stu-id="99b17-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="99b17-107">**WZCRefreshInterface** 函式會更新特定無線區域網路介面的介面資訊。</span><span class="sxs-lookup"><span data-stu-id="99b17-107">The **WZCRefreshInterface** function refreshes interface information for a specific wireless LAN interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="99b17-108">語法</span><span class="sxs-lookup"><span data-stu-id="99b17-108">Syntax</span></span>


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a><span data-ttu-id="99b17-109">參數</span><span class="sxs-lookup"><span data-stu-id="99b17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99b17-110">*pSrvAddr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b17-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b17-111">字串的指標，其中包含要在其上執行此函式的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="99b17-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="99b17-112">如果此參數為 **Null**，則會在本機電腦上呼叫無線零設定服務。</span><span class="sxs-lookup"><span data-stu-id="99b17-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is called on the local computer.</span></span>

<span data-ttu-id="99b17-113">如果指定的 *pSrvAddr* 參數是遠端電腦，則遠端電腦必須支援遠端 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="99b17-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="99b17-114">*dwInFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b17-114">*dwInFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b17-115">一組要重新整理的欄位，以及要採取的特定重新整理動作。</span><span class="sxs-lookup"><span data-stu-id="99b17-115">A set of fields to be refreshed along with specific refresh actions to be taken.</span></span> <span data-ttu-id="99b17-116">這是位元遮罩，可包含下列旗標的任何組合。</span><span class="sxs-lookup"><span data-stu-id="99b17-116">This is a bitmask that can contain any combination of the following flags.</span></span>



| <span data-ttu-id="99b17-117">值</span><span class="sxs-lookup"><span data-stu-id="99b17-117">Value</span></span>                                                                                                                                                                                                                            | <span data-ttu-id="99b17-118">意義</span><span class="sxs-lookup"><span data-stu-id="99b17-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <span data-ttu-id="99b17-119"><dt>**INTF \_描述**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-119"><dt>**INTF\_DESCR**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="99b17-120">重新整理無線區域網路介面的介面描述。</span><span class="sxs-lookup"><span data-stu-id="99b17-120">Refresh the interface description for a wireless LAN interface.</span></span><br/> <span data-ttu-id="99b17-121">您可以呼叫 [**WZCQueryInterface**](wzcqueryinterface.md)函式，並在 *dwInFlags* 參數中設定 **INTF \_ 描述** 位，以抓取重新整理的介面描述。</span><span class="sxs-lookup"><span data-stu-id="99b17-121">The refreshed interface description can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_DESCR** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="99b17-122">介面描述會傳回給 **WZCQueryInterface** 函數所傳回之 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszDescr** 成員。</span><span class="sxs-lookup"><span data-stu-id="99b17-122">The interface description is returned in the **wszDescr** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <span data-ttu-id="99b17-123"><dt>**INTF \_NDISMEDIA**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-123"><dt>**INTF\_NDISMEDIA**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="99b17-124">重新整理無線區域網路介面的 NDIS 媒體資訊。</span><span class="sxs-lookup"><span data-stu-id="99b17-124">Refresh the NDIS media information for a wireless LAN interface.</span></span><br/> <span data-ttu-id="99b17-125">您可以呼叫 [**WZCQueryInterface**](wzcqueryinterface.md)函式，並在 *dwInFlags* 參數中設定 **INTF \_ NDISMEDIA** 位，以抓取重新整理的 NDIS 媒體資訊。</span><span class="sxs-lookup"><span data-stu-id="99b17-125">The refreshed NDIS media information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function with the **INTF\_NDISMEDIA** bit set in the *dwInFlags* parameter.</span></span> <span data-ttu-id="99b17-126">在 **pIntf** 函式所傳回 *WZCQueryInterface* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **ulMediaState**、 **ulMediaType** 和 **ulPhysicalMediaType** 成員中，會傳回 NDIS 媒體資訊。</span><span class="sxs-lookup"><span data-stu-id="99b17-126">The NDIS media information is returned in the **ulMediaState**, **ulMediaType**, and **ulPhysicalMediaType** members of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter that is returned by the **WZCQueryInterface** function.</span></span><br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <span data-ttu-id="99b17-127"><dt>**INTF \_所有 \_ oid**</dt> <dt>0xFFF00000</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-127"><dt>**INTF\_ALL\_OIDS**</dt> <dt>0xFFF00000</dt></span></span> </dl>   | <span data-ttu-id="99b17-128">重新整理無線區域網路介面的所有 NDIS Oid。</span><span class="sxs-lookup"><span data-stu-id="99b17-128">Refresh all of the NDIS OIDs for a wireless LAN interface.</span></span> <span data-ttu-id="99b17-129">此選項會更新無線區域網路介面的大部分資料。</span><span class="sxs-lookup"><span data-stu-id="99b17-129">This option refreshes most of the data for a wireless LAN interface.</span></span><br/> <span data-ttu-id="99b17-130">您可以藉由呼叫 [**WZCQueryInterface**](wzcqueryinterface.md) 函式來取出重新整理的資訊。</span><span class="sxs-lookup"><span data-stu-id="99b17-130">The refreshed information can be retrieved by calling the [**WZCQueryInterface**](wzcqueryinterface.md) function.</span></span><br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="99b17-131">*pIntf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99b17-131">*pIntf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99b17-132">[**INTF \_ 專案**](intf-entry.md)結構的指標，其中包含要重新整理之介面的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="99b17-132">A pointer to an [**INTF\_ENTRY**](intf-entry.md) structure that contains the key of the interface to be refreshed.</span></span>

</dd> <dt>

<span data-ttu-id="99b17-133">*pdwOutFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="99b17-133">*pdwOutFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99b17-134">已成功重新整理的一組欄位。</span><span class="sxs-lookup"><span data-stu-id="99b17-134">A set of fields that were successfully refreshed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99b17-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="99b17-135">Return value</span></span>

<span data-ttu-id="99b17-136">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="99b17-136">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="99b17-137">如果函式失敗，則傳回值可能是下列其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="99b17-137">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="99b17-138">傳回碼</span><span class="sxs-lookup"><span data-stu-id="99b17-138">Return code</span></span>                                                                                              | <span data-ttu-id="99b17-139">Description</span><span class="sxs-lookup"><span data-stu-id="99b17-139">Description</span></span>                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="99b17-140"><dt>**錯誤 \_ 領域 \_ 垃圾桶**</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-140"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>     | <span data-ttu-id="99b17-141">儲存體控制區塊已損毀。</span><span class="sxs-lookup"><span data-stu-id="99b17-141">The storage control blocks were destroyed.</span></span> <span data-ttu-id="99b17-142">如果無線零設定服務尚未初始化內建物件，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="99b17-142">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="99b17-143"><dt>**\_ \_ \_ 找不到錯誤檔案**</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-143"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>   | <span data-ttu-id="99b17-144">系統找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="99b17-144">The system cannot find the file specified.</span></span> <span data-ttu-id="99b17-145">如果 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszGuid** 成員中的 GUID 與本機電腦上的任何無線區域網路介面不相符，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="99b17-145">This error is returned if the GUID in the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter did not match any of the wireless LAN interfaces on the local computer.</span></span> <br/> |
| <dl> <span data-ttu-id="99b17-146"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-146"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="99b17-147">參數不正確。</span><span class="sxs-lookup"><span data-stu-id="99b17-147">A parameter is incorrect.</span></span> <span data-ttu-id="99b17-148">如果 *pIntf* 參數為 **Null**，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="99b17-148">This error is returned if the *pIntf* parameter is **NULL**.</span></span> <span data-ttu-id="99b17-149">如果 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszGuid** 成員為 **Null**，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="99b17-149">This error is returned if the **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter is **NULL**.</span></span> <br/>                            |
| <dl> <span data-ttu-id="99b17-150"><dt>**RPC \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-150"><dt>**RPC\_STATUS**</dt></span></span> </dl>               | <span data-ttu-id="99b17-151">不同的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99b17-151">Various error codes.</span></span><br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="99b17-152">備註</span><span class="sxs-lookup"><span data-stu-id="99b17-152">Remarks</span></span>

<span data-ttu-id="99b17-153">*PIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **WSZGUID** 成員，必須包含無線區域網路介面的介面 GUID。</span><span class="sxs-lookup"><span data-stu-id="99b17-153">The **wszGuid** member of the [**INTF\_ENTRY**](intf-entry.md) structure pointed to by the *pIntf* parameter must contain an interface GUID for a wireless LAN interface.</span></span> <span data-ttu-id="99b17-154">您可以藉由呼叫 [**WZCEnumInterfaces**](wzcenuminterfaces.md) 函式來取出無線區域網路介面清單。</span><span class="sxs-lookup"><span data-stu-id="99b17-154">A list of wireless LAN interfaces can be retrieved by calling the [**WZCEnumInterfaces**](wzcenuminterfaces.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="99b17-155">Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔和 *Wzcsapi .lib* 匯入程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="99b17-155">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99b17-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="99b17-156">Requirements</span></span>



| <span data-ttu-id="99b17-157">需求</span><span class="sxs-lookup"><span data-stu-id="99b17-157">Requirement</span></span> | <span data-ttu-id="99b17-158">值</span><span class="sxs-lookup"><span data-stu-id="99b17-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99b17-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99b17-159">Minimum supported client</span></span><br/> | <span data-ttu-id="99b17-160">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99b17-160">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99b17-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99b17-161">Minimum supported server</span></span><br/> | <span data-ttu-id="99b17-162">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99b17-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="99b17-163">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="99b17-163">End of client support</span></span><br/>    | <span data-ttu-id="99b17-164">Windows XP （含 SP3）</span><span class="sxs-lookup"><span data-stu-id="99b17-164">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="99b17-165">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="99b17-165">End of server support</span></span><br/>    | <span data-ttu-id="99b17-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="99b17-166">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="99b17-167">標頭</span><span class="sxs-lookup"><span data-stu-id="99b17-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="99b17-168"><dt>Wzcsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-168"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="99b17-169">程式庫</span><span class="sxs-lookup"><span data-stu-id="99b17-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="99b17-170"><dt>Wzcsapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-170"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="99b17-171">DLL</span><span class="sxs-lookup"><span data-stu-id="99b17-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99b17-172"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99b17-172"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99b17-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99b17-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99b17-174">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="99b17-174">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="99b17-175">**WZCEnumInterfaces**</span><span class="sxs-lookup"><span data-stu-id="99b17-175">**WZCEnumInterfaces**</span></span>](wzcenuminterfaces.md)
</dt> <dt>

[<span data-ttu-id="99b17-176">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="99b17-176">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="99b17-177">**INTF \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="99b17-177">**INTF\_ENTRY**</span></span>](intf-entry.md)
</dt> </dl>

 

 




