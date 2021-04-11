---
description: Win32 \_ LogicalDiskToPartition 關聯 WMI 類別會建立邏輯磁片磁碟機及其所在磁碟分割的關聯。
ms.assetid: 41161d57-d392-4acc-a22a-10be75aa14a6
ms.tgt_platform: multiple
title: Win32_LogicalDiskToPartition 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskToPartition
- Win32_LogicalDiskToPartition.EndingAddress
- Win32_LogicalDiskToPartition.StartingAddress
- Win32_LogicalDiskToPartition.Antecedent
- Win32_LogicalDiskToPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a32a3ee275c32dde7d9f1484aa99dddeaf97a2e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110161"
---
# <a name="win32_logicaldisktopartition-class"></a><span data-ttu-id="fa133-103">Win32 \_ LogicalDiskToPartition 類別</span><span class="sxs-lookup"><span data-stu-id="fa133-103">Win32\_LogicalDiskToPartition class</span></span>

<span data-ttu-id="fa133-104">**Win32 \_ LogicalDiskToPartition** 關聯 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)會建立邏輯磁片磁碟機及其所在磁碟分割的關聯。</span><span class="sxs-lookup"><span data-stu-id="fa133-104">The **Win32\_LogicalDiskToPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk drive and the disk partition it resides on.</span></span>

<span data-ttu-id="fa133-105">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="fa133-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fa133-106">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="fa133-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa133-107">語法</span><span class="sxs-lookup"><span data-stu-id="fa133-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LogicalDiskToPartition : CIM_LogicalDiskBasedOnPartition
{
  uint64                  EndingAddress;
  uint64                  StartingAddress;
  Win32_DiskPartition REF Antecedent;
  Win32_LogicalDisk   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fa133-108">成員</span><span class="sxs-lookup"><span data-stu-id="fa133-108">Members</span></span>

<span data-ttu-id="fa133-109">**Win32 \_ LogicalDiskToPartition** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="fa133-109">The **Win32\_LogicalDiskToPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="fa133-110">屬性</span><span class="sxs-lookup"><span data-stu-id="fa133-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa133-111">屬性</span><span class="sxs-lookup"><span data-stu-id="fa133-111">Properties</span></span>

<span data-ttu-id="fa133-112">**Win32 \_ LogicalDiskToPartition** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="fa133-112">The **Win32\_LogicalDiskToPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa133-113">**先行**</span><span class="sxs-lookup"><span data-stu-id="fa133-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa133-114">資料類型： **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="fa133-114">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="fa133-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa133-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa133-116">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI \| Win32 \_ DiskPartition" ) </span><span class="sxs-lookup"><span data-stu-id="fa133-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="fa133-117">代表邏輯磁片所在之磁碟分割的屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="fa133-117">Reference to the instance representing the properties of a disk partition where the logical disk resides.</span></span>

</dd> <dt>

<span data-ttu-id="fa133-118">**依賴**</span><span class="sxs-lookup"><span data-stu-id="fa133-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa133-119">資料類型： **Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="fa133-119">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="fa133-120">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa133-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa133-121">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「WMI \| Win32 LogicalDisk」 \_ ) </span><span class="sxs-lookup"><span data-stu-id="fa133-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="fa133-122">代表位於實體磁碟分割上的邏輯磁片屬性之實例的參考。</span><span class="sxs-lookup"><span data-stu-id="fa133-122">Reference to the instance representing the properties of a logical disk that resides on a physical disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="fa133-123">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="fa133-123">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa133-124">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fa133-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa133-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa133-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa133-126">指出較低層級儲存體中的高階範圍結尾。</span><span class="sxs-lookup"><span data-stu-id="fa133-126">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="fa133-127">當將非連續的範圍對應至較高層級的群組時，這個屬性會很有用。</span><span class="sxs-lookup"><span data-stu-id="fa133-127">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="fa133-128">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="fa133-128">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fa133-129">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="fa133-129">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa133-130">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="fa133-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa133-131">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="fa133-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fa133-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="fa133-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa133-133">表示較低層級儲存體中的高階範圍開始。</span><span class="sxs-lookup"><span data-stu-id="fa133-133">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="fa133-134">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="fa133-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="fa133-135">這個屬性繼承自 [**CIM \_ BasedOn**](cim-basedon.md)。</span><span class="sxs-lookup"><span data-stu-id="fa133-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa133-136">備註</span><span class="sxs-lookup"><span data-stu-id="fa133-136">Remarks</span></span>

<span data-ttu-id="fa133-137">**Win32 \_ LogicalDiskToPartition** 類別衍生自 [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)。</span><span class="sxs-lookup"><span data-stu-id="fa133-137">The **Win32\_LogicalDiskToPartition** class is derived from [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md).</span></span>

<span data-ttu-id="fa133-138">如需邏輯磁碟機與實體磁片之間對應的詳細資訊，請參閱 [如何將邏輯磁碟機和實體磁片相互關聯？](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fa133-138">For more information on mapping between a logical drive and a physical disk, see [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx).</span></span>

## <a name="examples"></a><span data-ttu-id="fa133-139">範例</span><span class="sxs-lookup"><span data-stu-id="fa133-139">Examples</span></span>

<span data-ttu-id="fa133-140">下列 c + + 程式碼範例說明如何取出指定磁片磁碟機的磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="fa133-140">The following C++ code sample describes how to retrieve the drive letters for a specified disk drive.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>


#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")


  
BOOL wmi_run();
BOOL wmi_getDriveLetters();
BOOL wmi_close();


  
IWbemLocator *pLoc = NULL;
IWbemServices *pSvc = NULL;


  
int main(int argc, char **argv)
{
    wmi_run();
    wmi_getDriveLetters();

    system("pause");
    wmi_close();
}


  
//
// Step 1-5 at:
// https://msdn.microsoft.com/library/aa390423(VS.85).aspx
BOOL wmi_run()
{
     HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------
    // Note: If you are using Windows 2000, you need to specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );


  
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }

    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    //IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);

    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    //IWbemServices *pSvc = NULL;

    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (e.g. Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
         );

    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;

    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }
 return 0;
}


  
//
// get Drives, logical Drives and Driveletters
BOOL wmi_getDriveLetters()
{

    // Use the IWbemServices pointer to make requests of WMI. 
    // Make requests here:
    HRESULT hres;
    IEnumWbemClassObject* pEnumerator = NULL;

    // get localdrives
    hres = pSvc->ExecQuery(
                    bstr_t("WQL"), 
                    bstr_t("SELECT * FROM Win32_DiskDrive"),
                    WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                    NULL,
                    &pEnumerator);

    if (FAILED(hres)) {
        cout << "Query for processes failed. "
             << "Error code = 0x" 
             << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return FALSE;               // Program has failed.
    }
    else { 

        IWbemClassObject *pclsObj;
        ULONG uReturn = 0;
        while (pEnumerator) {
           hres = pEnumerator->Next(WBEM_INFINITE, 1, 
                                 &pclsObj, &uReturn);
           if(0 == uReturn) break;

           VARIANT vtProp;
           hres = pclsObj->Get(_bstr_t(L"DeviceID"), 0, &vtProp, 0, 0);

           // adjust string
           wstring tmp = vtProp.bstrVal;
           tmp = tmp.substr(4);

           wstring wstrQuery = L"Associators of {Win32_DiskDrive.DeviceID='\\\\.\\";
           wstrQuery += tmp;
           wstrQuery += L"'} where AssocClass=Win32_DiskDriveToDiskPartition";

           // reference drive to partition
           IEnumWbemClassObject* pEnumerator1 = NULL;
           hres = pSvc->ExecQuery(
                             bstr_t("WQL"), 
                             bstr_t( wstrQuery.c_str()),
                             WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                             NULL,
                             &pEnumerator1 );

           if ( FAILED(hres) ) {
            cout << "Query for processes failed. "
                          << "Error code = 0x" 
                          << hex << hres << endl;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return FALSE;               // Program has failed.
           } else {

                IWbemClassObject *pclsObj1;
                ULONG uReturn1 = 0;
                while( pEnumerator1 ) {
                     hres = pEnumerator1->Next( WBEM_INFINITE, 1, 
                     &pclsObj1, &uReturn1 );
                     if(0 == uReturn1) break;

                     // reference logical drive to partition
                     VARIANT vtProp1;
                     hres = pclsObj1->Get( _bstr_t(L"DeviceID"), 0, &vtProp1, 0, 0 );
                     wstring wstrQuery = L"Associators of {Win32_DiskPartition.DeviceID='";
                     wstrQuery += vtProp1.bstrVal;
                     wstrQuery += L"'} where AssocClass=Win32_LogicalDiskToPartition";


  
                     IEnumWbemClassObject* pEnumerator2 = NULL;
                     hres = pSvc->ExecQuery(
                                       bstr_t("WQL"), 
                                       bstr_t(wstrQuery.c_str()),
                                       WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
                                       NULL,
                                       &pEnumerator2 );





                    if ( FAILED(hres) ) {
                        cout << "Query for processes failed. "
                                << "Error code = 0x" 
                                << hex << hres << endl;
                        pSvc->Release();
                        pLoc->Release();     
                        CoUninitialize();
                        return FALSE;               // Program has failed.
                     } else {

                        // get driveletter
                        IWbemClassObject *pclsObj2;
                        ULONG uReturn2 = 0;
                        while( pEnumerator2 ) {
                            hres = pEnumerator2->Next( WBEM_INFINITE, 1, 
                            &pclsObj2, &uReturn2 );
                            if(0 == uReturn2) break;

                            VARIANT vtProp2;
                            hres = pclsObj2->Get( _bstr_t(L"DeviceID"), 0, &vtProp2, 0, 0 );


  
                            // print result
                            printf("%ls : %ls\n", vtProp.bstrVal, vtProp2.bstrVal);

                            VariantClear( &vtProp2 );
                        }
                        pclsObj1->Release();
                    }
                    VariantClear( &vtProp1 );
                    pEnumerator2->Release();
                }
                pclsObj->Release();
            }
            VariantClear( &vtProp );
            pEnumerator1->Release();
        }
     }
     pEnumerator->Release();
     return TRUE;
}






BOOL wmi_close()
{
 // Cleanup
    // ========

    pSvc->Release();
    pLoc->Release();
    CoUninitialize();

    return 0;   // Program successfully completed. 
}
```



## <a name="requirements"></a><span data-ttu-id="fa133-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa133-141">Requirements</span></span>



| <span data-ttu-id="fa133-142">需求</span><span class="sxs-lookup"><span data-stu-id="fa133-142">Requirement</span></span> | <span data-ttu-id="fa133-143">值</span><span class="sxs-lookup"><span data-stu-id="fa133-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa133-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa133-144">Minimum supported client</span></span><br/> | <span data-ttu-id="fa133-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa133-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa133-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa133-146">Minimum supported server</span></span><br/> | <span data-ttu-id="fa133-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa133-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa133-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa133-148">Namespace</span></span><br/>                | <span data-ttu-id="fa133-149">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fa133-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa133-150">MOF</span><span class="sxs-lookup"><span data-stu-id="fa133-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa133-151"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa133-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa133-152">DLL</span><span class="sxs-lookup"><span data-stu-id="fa133-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa133-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa133-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa133-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa133-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa133-155">**CIM \_ LogicalDiskBasedOnPartition**</span><span class="sxs-lookup"><span data-stu-id="fa133-155">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dt>

<span data-ttu-id="fa133-156">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fa133-156">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fa133-157">WMI 工作：磁片和檔案系統</span><span class="sxs-lookup"><span data-stu-id="fa133-157">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

