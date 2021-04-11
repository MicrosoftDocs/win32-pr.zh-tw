---
description: 列舉無線零設定服務所管理的所有無線區域網路介面。
ms.assetid: ef8a6a3e-042a-4219-baed-a82bb3e983ae
title: 'WZCEnumInterfaces 函式 (Wzcsapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEnumInterfaces
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: b2a2c886f59843dd1bf1316053c603faf4cc112a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851784"
---
# <a name="wzcenuminterfaces-function"></a><span data-ttu-id="a2ed4-103">WZCEnumInterfaces 函式</span><span class="sxs-lookup"><span data-stu-id="a2ed4-103">WZCEnumInterfaces function</span></span>

<span data-ttu-id="a2ed4-104">\[Windows Vista 和 Windows Server 2008 已不再支援 **WZCEnumInterfaces** 。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-104">\[**WZCEnumInterfaces** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="a2ed4-105">請改用 [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) 函數。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-105">Instead, use the [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) function.</span></span> <span data-ttu-id="a2ed4-106">如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]</span><span class="sxs-lookup"><span data-stu-id="a2ed4-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="a2ed4-107">**WZCEnumInterfaces** 函式會列舉無線零設定服務所管理的所有無線區域網路介面。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-107">The **WZCEnumInterfaces** function enumerates all of the wireless LAN interfaces managed by the Wireless Zero Configuration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ed4-108">語法</span><span class="sxs-lookup"><span data-stu-id="a2ed4-108">Syntax</span></span>


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a><span data-ttu-id="a2ed4-109">參數</span><span class="sxs-lookup"><span data-stu-id="a2ed4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ed4-110">*pSrvAddr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a2ed4-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ed4-111">字串的指標，其中包含要在其上執行此函式的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="a2ed4-112">如果此參數為 **Null**，則會在本機電腦上列舉無線零設定服務。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is enumerated on the local computer.</span></span>

<span data-ttu-id="a2ed4-113">如果指定的 *pSrvAddr* 參數是遠端電腦，則遠端電腦必須支援遠端 RPC 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="a2ed4-114">*pIntfs* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a2ed4-114">*pIntfs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ed4-115">[**INTFS 索引 \_ 鍵 \_ 資料表**](intfs-key-table.md)結構的指標，其中包含所有介面的索引鍵資訊資料表。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-115">A pointer to a [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure that contains a table of key information for all interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ed4-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2ed4-116">Return value</span></span>

<span data-ttu-id="a2ed4-117">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a2ed4-118">如果函式失敗，則傳回值可能是下列其中一個傳回碼。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-118">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="a2ed4-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a2ed4-119">Return code</span></span>                                                                                               | <span data-ttu-id="a2ed4-120">Description</span><span class="sxs-lookup"><span data-stu-id="a2ed4-120">Description</span></span>                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2ed4-121"><dt>**錯誤 \_ 領域 \_ 垃圾桶**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed4-121"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="a2ed4-122">儲存體控制區塊已損毀。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-122">The storage control blocks were destroyed.</span></span> <span data-ttu-id="a2ed4-123">如果無線零設定服務尚未初始化內建物件，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-123">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/> |
| <dl> <span data-ttu-id="a2ed4-124"><dt>**RPC \_ \_ 未知（ \_ 如果**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed4-124"><dt>**RPC\_S\_UNKNOWN\_IF**</dt></span></span> </dl>        | <span data-ttu-id="a2ed4-125">介面未知。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-125">The interface is unknown.</span></span><br/> <span data-ttu-id="a2ed4-126">如果未啟動無線零設定服務，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-126">This error is returned if the Wireless Zero Configuration service is not started.</span></span><br/>                             |
| <dl> <span data-ttu-id="a2ed4-127"><dt>**RPC \_ X \_ Null \_ REF \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed4-127"><dt>**RPC\_X\_NULL\_REF\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="a2ed4-128">傳遞給存根的 null 參考指標。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-128">A null reference pointer was passed to the stub.</span></span><br/> <span data-ttu-id="a2ed4-129">如果 *pIntfs* 參數為 **Null**，就會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-129">This error is returned if the *pIntfs* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="a2ed4-130"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed4-130"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="a2ed4-131">沒有足夠的記憶體可用來處理此要求，並配置記憶體給查詢結果。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-131">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="a2ed4-132"><dt>**RPC \_ 狀態**</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed4-132"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="a2ed4-133">不同的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-133">Various error codes.</span></span><br/>                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="a2ed4-134">備註</span><span class="sxs-lookup"><span data-stu-id="a2ed4-134">Remarks</span></span>

<span data-ttu-id="a2ed4-135">*PIntf* 所指向之 [**INTFS 索引 \_ 鍵 \_ 資料表**](intfs-key-table.md)結構的 **dwNumIntfs** 成員必須先設定為0，然後再呼叫 **WZCEnumInterfaces** 函數。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-135">The **dwNumIntfs** member of the [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure pointed to by *pIntf* must be set to 0 before calling the **WZCEnumInterfaces** function.</span></span> <span data-ttu-id="a2ed4-136">此外， **pIntfs** 成員必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-136">Also, the **pIntfs** member must be set to **NULL**.</span></span>

<span data-ttu-id="a2ed4-137">針對其他無線零設定函式的後續呼叫，應用程式必須提供 **WZCEnumInterfaces** 函式所傳回的相關索引鍵資訊，以識別其正在運作的介面。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-137">For subsequent calls to other Wireless Zero Configuration functions, an application must identify the interface it is operating on by providing relevant key information returned by the **WZCEnumInterfaces** function.</span></span>

<span data-ttu-id="a2ed4-138">如果 **WZCEnumInterfaces** 傳回錯誤 \_ 成功，呼叫端應該呼叫 [**>localfree**](/windows/win32/api/winbase/nf-winbase-localfree) 來釋出針對所傳回之資料所配置的內部緩衝區，而不再需要這項資訊。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-138">If the **WZCEnumInterfaces** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="a2ed4-139">Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔和 *Wzcsapi .lib* 匯入程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-139">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="examples"></a><span data-ttu-id="a2ed4-140">範例</span><span class="sxs-lookup"><span data-stu-id="a2ed4-140">Examples</span></span>

<span data-ttu-id="a2ed4-141">下列範例會列舉無線零設定服務所管理之本機電腦上的無線區域網路介面，並印出每個介面的介面 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-141">The following example enumerates the wireless LAN interfaces on the local computer managed by the Wireless Zero Configuration service and prints out the value for interface GUID for each interface.</span></span>

> [!Note]  
> <span data-ttu-id="a2ed4-142">在 Windows Vista 和更新版本上，此範例將會失敗。</span><span class="sxs-lookup"><span data-stu-id="a2ed4-142">This example will fail on Windows Vista and later .</span></span>

 


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <objbase.h>
#include <wtypes.h>

#include <stdio.h>
#include <stdlib.h>

// Wzcsapi.h and Wsczapi.lib were never shipped
// So we need to LOadlibrary and call the WZCEnumInterfaces function 
// in Wzcsapi.dll in the 

typedef struct
{
    LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;

typedef struct
{
    DWORD dwNumIntfs;
    PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;

DWORD WZCEnumInterfaces(LPWSTR pSrvAddr, PINTFS_KEY_TABLE pIntfs);

//Define the function prototype
typedef DWORD (CALLBACK* WZCEnumInterfacesType)(LPWSTR, PINTFS_KEY_TABLE);

int wmain()
{
    // Declare and initialize variables.

    DWORD dwResult = 0;
//    int iRet = 0;
    
//    WCHAR GuidString[40] = {0};
     
    int i;

    /* variables used for WZCEnumInterfaces  */
    
    PINTFS_KEY_TABLE pIfList; 
    PINTF_KEY_ENTRY pIfInfo;
    
    BOOL freeResult = FALSE;
    BOOL runTimeLinkSuccess = FALSE; 
    HINSTANCE dllHandle = NULL;              
    WZCEnumInterfacesType WZCEnumInterfacesPtr = NULL;

//    wprintf(L"Sample to test WZCEnumInterface\n");
    
    //Load the dll and keep the handle to it
    dllHandle = LoadLibrary( (LPCWSTR) L"wzcsapi.dll");

    // If the handle is valid, try to get the function address. 
    if (dllHandle == NULL) {
        dwResult = GetLastError();
        wprintf(L"LoadLibrary of wzcsapi.dll failed with error: %d\n", dwResult);
        if (dwResult ==  ERROR_MOD_NOT_FOUND)
            wprintf(L"Error: The specified module could not be found\n");
        return 1;
    }
    else  
    { 
        //Get pointer to our function using GetProcAddress:
        WZCEnumInterfacesPtr = (WZCEnumInterfacesType) GetProcAddress(dllHandle,
         "WZCEnumInterfaces");

        if (WZCEnumInterfacesPtr != NULL)
            runTimeLinkSuccess = TRUE;
        else {
            dwResult = GetLastError();   
            wprintf(L"GetProcAddress of WZCEnumInterfaces failed with error: %d\n", dwResult);
            return 1;
        }    
             
        // The function address is valid, allocate some memory for pIflist
        pIfList = (PINTFS_KEY_TABLE) LocalAlloc(LMEM_ZEROINIT,4096);
        if (pIfList == NULL) {    
            wprintf(L"Unable to allocate memory to store INTFS_KEY_TABLE\n");
            freeResult = FreeLibrary(dllHandle);
            return 1;
        }    

        // If the function address is valid, call the function. 
        if (runTimeLinkSuccess)
        {
            dwResult = WZCEnumInterfacesPtr(NULL, pIfList); 
            if (dwResult != ERROR_SUCCESS)  {
                wprintf(L"WZCEnumInterfaces failed with error: %u\n", dwResult);
                // FormatMessage can be used to find out why the function failed
                  //Free the library:
                freeResult = FreeLibrary(dllHandle);
                return 1;
            }
            else {
                wprintf(L"Num Entries: %lu\n", pIfList->dwNumIntfs);

                for (i = 0; i < (int) pIfList->dwNumIntfs; i++) {
                    pIfInfo = &pIfList->pIntfs[i];
                    if (pIfInfo->wszGuid == NULL)
                        wprintf(L"  InterfaceGUID[%d]: NULL\n",i);
                    else
                        wprintf(L"  InterfaceGUID[%d]: %ws\n",i, pIfInfo->wszGuid);
                    
                }    
            }
            wprintf(L"\n");
        }
        
        freeResult = FreeLibrary(dllHandle);
    }

    if (pIfList != NULL) {
        LocalFree(pIfList);
        pIfList = NULL;
    }
    return 0;
}
```



## <a name="requirements"></a><span data-ttu-id="a2ed4-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2ed4-143">Requirements</span></span>



| <span data-ttu-id="a2ed4-144">需求</span><span class="sxs-lookup"><span data-stu-id="a2ed4-144">Requirement</span></span> | <span data-ttu-id="a2ed4-145">值</span><span class="sxs-lookup"><span data-stu-id="a2ed4-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ed4-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a2ed4-146">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ed4-147">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2ed4-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a2ed4-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a2ed4-148">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ed4-149">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a2ed4-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a2ed4-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a2ed4-150">End of client support</span></span><br/>    | <span data-ttu-id="a2ed4-151">Windows XP （含 SP3）</span><span class="sxs-lookup"><span data-stu-id="a2ed4-151">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="a2ed4-152">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a2ed4-152">End of server support</span></span><br/>    | <span data-ttu-id="a2ed4-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a2ed4-153">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a2ed4-154">標頭</span><span class="sxs-lookup"><span data-stu-id="a2ed4-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ed4-155"><dt>Wzcsapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed4-155"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="a2ed4-156">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2ed4-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2ed4-157"><dt>Wzcsapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed4-157"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a2ed4-158">DLL</span><span class="sxs-lookup"><span data-stu-id="a2ed4-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2ed4-159"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ed4-159"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2ed4-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2ed4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ed4-161">**INTFS 索引 \_ 鍵 \_ 資料表**</span><span class="sxs-lookup"><span data-stu-id="a2ed4-161">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="a2ed4-162">**INTF \_ 金鑰 \_ 專案**</span><span class="sxs-lookup"><span data-stu-id="a2ed4-162">**INTF\_KEY\_ENTRY**</span></span>](intf-key-entry.md)
</dt> <dt>

[<span data-ttu-id="a2ed4-163">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="a2ed4-163">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="a2ed4-164">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="a2ed4-164">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="a2ed4-165">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="a2ed4-165">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
