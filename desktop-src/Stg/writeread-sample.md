---
title: WriteRead 範例
description: WriteRead 會建立屬性集、寫入屬性、關閉和重新開啟屬性集，然後再讀取屬性。
ms.assetid: c5807dd9-2928-497b-9446-729dcaeebc8a
keywords:
- 結構化儲存體 Strctd Stg.、範例、WriteRead
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362af8665f56e1dc8d7909fb1363e3e0ee7a8136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673959"
---
# <a name="writeread-sample"></a><span data-ttu-id="d39ea-104">WriteRead 範例</span><span class="sxs-lookup"><span data-stu-id="d39ea-104">WriteRead Sample</span></span>

<span data-ttu-id="d39ea-105">WriteRead 會建立屬性集、寫入屬性、關閉和重新開啟屬性集，然後再讀取屬性。</span><span class="sxs-lookup"><span data-stu-id="d39ea-105">The WriteRead.cpp creates a property set, writes a property, closes and reopens the property set, and reads back the property.</span></span> <span data-ttu-id="d39ea-106">這個範例應用程式會在目前的目錄中建立 "WriteRead. stg." 檔案。</span><span class="sxs-lookup"><span data-stu-id="d39ea-106">This sample application creates the file "WriteRead.stg" in the current directory.</span></span> <span data-ttu-id="d39ea-107">它會在結構儲存體檔案中建立屬性集，但單行變更會導致它建立 NTFS 檔案系統屬性集。</span><span class="sxs-lookup"><span data-stu-id="d39ea-107">It creates property sets in a structure storage file, but a one-line change causes it to create NTFS file system property sets.</span></span>


```C++
//+===================================================================
//
//      To build:
//      cl /GX WriteRead.cpp
//
//+===================================================================


#define WIN32_LEAN_AND_MEAN
#define UNICODE
#define _UNICODE

#include <stdio.h>
#include <windows.h>
#include <ole2.h>

// Implicitly link ole32.dll
#pragma comment( lib, "ole32.lib" )


// From uuidgen.exe:
const FMTID fmtid = { /* d170df2e-1117-11d2-aa01-00805ffe11b8 */
    0xd170df2e,
    0x1117,
    0x11d2,
    {0xaa, 0x01, 0x00, 0x80, 0x5f, 0xfe, 0x11, 0xb8}
  };


EXTERN_C void wmain()
{
   HRESULT hr = S_OK;
   IPropertySetStorage *pPropSetStg = NULL;
   IPropertyStorage *pPropStg = NULL;
   WCHAR *pwszError = L"";
   PROPSPEC propspec; 
   PROPVARIANT propvarWrite; 
   PROPVARIANT propvarRead;

   try
   {

        // Create a file and a property set within it.

        hr = StgCreateStorageEx( L"WriteRead.stg",
                   STGM_CREATE|STGM_SHARE_EXCLUSIVE|STGM_READWRITE,
                   STGFMT_STORAGE,
                   // STGFMT_STORAGE => Structured Storage 
                                     // property sets
                   // STGFMT_FILE    => NTFS file system 
                                     // property sets
                   0, NULL, NULL,
                   IID_IPropertySetStorage,
                   reinterpret_cast<void**>(&pPropSetStg) );
        if( FAILED(hr) ) throw L"Failed StgCreateStorageEx";

        hr = pPropSetStg->Create( fmtid, NULL, PROPSETFLAG_DEFAULT, 
                    STGM_CREATE|STGM_READWRITE|STGM_SHARE_EXCLUSIVE,
                    &pPropStg );
        if( FAILED(hr) ) throw L"Failed IPropertySetStorage::Create";

        // Write a Unicode string property to the property set

        propspec.ulKind = PRSPEC_LPWSTR;
        propspec.lpwstr = L"Property Name";

        propvarWrite.vt = VT_LPWSTR;
        propvarWrite.pwszVal = L"Property Value";

        hr = pPropStg->WriteMultiple( 1, &propspec, &propvarWrite, 
                                      PID_FIRST_USABLE );
        if( FAILED(hr) ) 
            throw L"Failed IPropertyStorage::WriteMultiple";

        // Not required, but give the property set a friendly 
        // name.

        PROPID propidDictionary = PID_DICTIONARY;
        WCHAR *pwszFriendlyName = 
                     L"Write/Read Properties Sample Property Set";
        hr = pPropStg->WritePropertyNames( 1, &propidDictionary, 
                                           &pwszFriendlyName );
        if( FAILED(hr) ) 
            throw L"Failed IPropertyStorage::WritePropertyNames";

        // Commit changes to the property set.

        hr = pPropStg->Commit(STGC_DEFAULT);
        if( FAILED(hr) ) 
            throw L"Failed IPropertyStorage::Commit";

        // Close and reopen everything.
        // By using the STGFMT_ANY flag in the StgOpenStorageEx call,
        // it does not matter if this is a Structured Storage 
        // property set or an NTFS file system property set 
        // (for more information see the StgCreateStorageEx 
        // call above).

        pPropStg->Release(); pPropStg = NULL;
        pPropSetStg->Release(); pPropSetStg = NULL;

        hr = StgOpenStorageEx( L"WriteRead.stg",
                             STGM_READ|STGM_SHARE_DENY_WRITE,
                             STGFMT_ANY,
                             0, NULL, NULL, 
                             IID_IPropertySetStorage,
                             reinterpret_cast<void**>(&pPropSetStg) );
        if( FAILED(hr) ) 
            throw L"Failed StgOpenStorageEx";

        hr = pPropSetStg->Open( fmtid, STGM_READ|STGM_SHARE_EXCLUSIVE,
                                &pPropStg );
        if( FAILED(hr) ) 
            throw L"Failed IPropertySetStorage::Open";

        // Read the property back and validate it

        hr = pPropStg->ReadMultiple( 1, &propspec, &propvarRead );
        if( FAILED(hr) ) 
            throw L"Failed IPropertyStorage::ReadMultiple";

        if( S_FALSE == hr )
          throw L"Property didn't exist after reopening the 
                                                     property set";
        else if( propvarWrite.vt != propvarRead.vt )
          throw L"Property types didn't match after reopening the 
                                                     property set";
        else if( 0 != wcscmp( propvarWrite.pwszVal, 
                              propvarRead.pwszVal ))
          throw L"Property values didn't match after reopening the 
                                                     property set";
        else
           wprintf( L"Success\n" );

   }
   catch( const WCHAR *pwszError )
   {
       wprintf( L"Error:  %s (hr=%08x)\n", pwszError, hr );
   }

   PropVariantClear( &propvarRead );
            if( pPropStg ) pPropStg->Release();
   if( pPropSetStg ) pPropSetStg->Release();

}
```



 

 




