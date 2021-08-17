---
description: 下列範例示範如何使用 GetNPPBlobTable 函式來取出 NPP BLOB 資料表，以代表本機電腦上已註冊的網路介面卡。
ms.assetid: 7267f658-103d-4290-8ebf-b78866bd1fe8
title: 使用 GetNPPBlobTable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5b31031ad18930c44bffe1efd980834f6c854b144f718891b66bd7df31b3f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962788"
---
# <a name="using-getnppblobtable"></a>使用 GetNPPBlobTable

下列範例示範如何使用 [**GetNPPBlobTable**](getnppblobtable.md) 函式來取出 NPP BLOB 資料表，以代表本機電腦上已註冊的網路介面卡。


```C++
DWORD rc;
PBLOB_TABLE pBlobTable;
// Create the filter blob
HBLOB hFilterBlob;
if (NMERR_SUCCESS != (rc = CreateBlob(&hFilterBlob)))
    return FALSE;

// Set test criteria
// To obtain delayed capture interface
if (NMERR_SUCCESS != (rc = SetBoolInBlob (
                             hFilterBlob,
                             OWNER_NPP,
                             CATEGORY_CONFIG,
                             TAG_INTERFACE_DELAYED_CAPTURE,
                             TRUE)))
    return FALSE;

// Only obtain Ethernet cards
if (NMERR_SUCCESS != (rc = SetStringInBlob(hBlob,
                             OWNER_NPP,
                             CATEGORY_NETWORKINFO,
                             TAG_MACTYPE,
                             PROTOCOL_STRING_ETHERNET_TXT)))
    return FALSE;

// To get SpecialBlobs back
if (NMERR_SUCCESS != (rc = SetBoolInBlob(hBlob,
                             OWNER_NPP,
                             CATEGORY_FINDER,
                             TAG_GET_SPECIAL_BLOBS,
                             TRUE)))
    return FALSE;

// Make the call to the finder
rc = GetNPPBlobTable( hFilterBlob, &pBlobTable );

// Did we get anything?
if (rc != NMERR_SUCCESS)
    return FALSE;


//  To obtain a "special" blob.
//  Should have set
//  the filter blob to include the TAG_INTERFACE_REMOTE
//  interface &#8211; then only a TAG_INTERFACE_REMOTE interface
//  would return.

HBLOB OurBlob = NULL;
DWORD index;
for (index = 0; index < pBlobTable->dwNumBlobs; index++)
{
    // Here is the test for a special blob
    if (NMERR_SUCCESS == 
       (rc = GetStringFromBlob(pBlobTable->Blobs[index],
                               OWNER_NPP,
                               CATEGORY_FINDER,
                               TAG_DLL_FILENAME,
                               &DLLFileName)))
    {
        // This is a special blob.
        // Check to see if it is supports the remote interface.
        BOOL bGoesRemote;
        rc = GetBoolFromBlob( hBlob,
                              OWNER_NPP,
                              CATEGORY_CONFIG,
                              TAG_INTERFACE_DELAYED_CAPTURE,
                              &bGoesRemote);
        if (rc == NMERR_SUCCESS && bGoesRemote)
        {
            // This is the one we want. Save it off
            OurBlob = pBlobTable->Blobs[index];
            break;
        }
    }
}

if (OurBlob == NULL)
    return FALSE;

// Set the computer name in our special blob.
rc = SetStringInBlob(OurBlob,
                     OWNER_NPP,
                     CATEGORY_LOCATION,
                     TAG_REMOTE_MACHINE_NAME,
                     "mycomputer");

PBLOB_TABLE pSecondBlobTable;
// Call the finder again.
rc = GetNPPBlobTable( OurBlob, &pSecondBlobTable );

// Did we get anything?
if (rc != NMERR_SUCCESS)
    return FALSE;

// A Blob is now on mycomputer.
// Use the blob as shown in the previous example.
```



 

 



