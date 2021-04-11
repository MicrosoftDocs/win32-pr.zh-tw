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
# <a name="wzcenuminterfaces-function"></a>WZCEnumInterfaces 函式

\[Windows Vista 和 Windows Server 2008 已不再支援 **WZCEnumInterfaces** 。 請改用 [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) 函數。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]

**WZCEnumInterfaces** 函式會列舉無線零設定服務所管理的所有無線區域網路介面。

## <a name="syntax"></a>語法


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrvAddr* \[在\]
</dt> <dd>

字串的指標，其中包含要在其上執行此函式的電腦名稱稱。 如果此參數為 **Null**，則會在本機電腦上列舉無線零設定服務。

如果指定的 *pSrvAddr* 參數是遠端電腦，則遠端電腦必須支援遠端 RPC 呼叫。

</dd> <dt>

*pIntfs* \[擴展\]
</dt> <dd>

[**INTFS 索引 \_ 鍵 \_ 資料表**](intfs-key-table.md)結構的指標，其中包含所有介面的索引鍵資訊資料表。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可能是下列其中一個傳回碼。



| 傳回碼                                                                                               | Description                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 領域 \_ 垃圾桶**</dt> </dl>      | 儲存體控制區塊已損毀。 如果無線零設定服務尚未初始化內建物件，則會傳回此錯誤。<br/> |
| <dl> <dt>**RPC \_ \_ 未知（ \_ 如果**</dt> </dl>        | 介面未知。<br/> 如果未啟動無線零設定服務，則會傳回此錯誤。<br/>                             |
| <dl> <dt>**RPC \_ X \_ Null \_ REF \_ 指標**</dt> </dl> | 傳遞給存根的 null 參考指標。<br/> 如果 *pIntfs* 參數為 **Null**，就會傳回此錯誤。<br/>                          |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl> | 沒有足夠的記憶體可用來處理此要求，並配置記憶體給查詢結果。<br/>                                                  |
| <dl> <dt>**RPC \_ 狀態**</dt> </dl>                | 不同的錯誤碼。<br/>                                                                                                                               |



 

## <a name="remarks"></a>備註

*PIntf* 所指向之 [**INTFS 索引 \_ 鍵 \_ 資料表**](intfs-key-table.md)結構的 **dwNumIntfs** 成員必須先設定為0，然後再呼叫 **WZCEnumInterfaces** 函數。 此外， **pIntfs** 成員必須設定為 **Null**。

針對其他無線零設定函式的後續呼叫，應用程式必須提供 **WZCEnumInterfaces** 函式所傳回的相關索引鍵資訊，以識別其正在運作的介面。

如果 **WZCEnumInterfaces** 傳回錯誤 \_ 成功，呼叫端應該呼叫 [**>localfree**](/windows/win32/api/winbase/nf-winbase-localfree) 來釋出針對所傳回之資料所配置的內部緩衝區，而不再需要這項資訊。

> [!Note]  
> Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔和 *Wzcsapi .lib* 匯入程式庫檔案。

 

## <a name="examples"></a>範例

下列範例會列舉無線零設定服務所管理之本機電腦上的無線區域網路介面，並印出每個介面的介面 GUID 值。

> [!Note]  
> 在 Windows Vista 和更新版本上，此範例將會失敗。

 


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP （含 SP3）<br/>                                                         |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Wzcsapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Wzcsapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INTFS 索引 \_ 鍵 \_ 資料表**](intfs-key-table.md)
</dt> <dt>

[**INTF \_ 金鑰 \_ 專案**](intf-key-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
