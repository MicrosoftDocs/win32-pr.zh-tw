---
description: 必須從安全性資料庫和服務中取出設定資訊，比較這兩組資訊，然後更新安全性資料庫的 [分析] 區段，並提供任何差異。
ms.assetid: f8420dde-55a2-40a0-b10d-140c28c0e9e4
title: 執行 SceSvcAttachmentAnalyze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1561449c88c31dd33eb1d16d2cb0ece854c5db0ea7d76503d872c8d4bbf797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894629"
---
# <a name="implementing-scesvcattachmentanalyze"></a>執行 SceSvcAttachmentAnalyze

[**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)函式必須從安全性資料庫和服務中取出設定資訊，比較這兩組資訊，然後更新安全性資料庫的 [分析] 區段，並提供任何差異。 您可以使用下列演算法來確定這一點。

**若要執行 SceSvcAttachmentAnalyze**

1.  定義取出及設定安全性資訊和傳回碼所需的變數。
2.  在回呼結構中呼叫 pfQueryInfo 回呼函式，以從安全性資料庫中取出設定資訊。
3.  從服務中取出對應的資訊。
4.  比較從服務中取出的設定資料與從安全性資料庫抓取的設定資料。
5.  如果資訊不同，請在回呼結構中呼叫 pfSetInfo 回呼函式來更新資料庫。
6.  釋放用來取得資訊的所有緩衝區。 在回呼結構中呼叫 pfFreeInfo 回呼函式，以釋放用於傳回之資料庫資訊的記憶體。
7.  如果有任何訊息要將擴充功能新增至分析記錄檔，請在回呼結構中呼叫 pfLogInfo 回呼函式。
8.  傳回適當的 **SCESTATUS** 碼。

下列範例顯示一個可能的 [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)執行。 請注意，在此範例中，QueryConfigurationLine 和 CompareValue 函式會分別從服務查詢資訊，並將這些值與從安全性資料庫抓取的值進行比較。 不會顯示這些函式的實作為。


```C++
#include <windows.h>

SCESTATUS WINAPI SceSvcAttachmentAnalyze (
    IN PSCESVC_CALLBACK_INFO pSceCbInfo
)
{
  
    ////////////////////////////////////////////////////
    // Define variables.
    ////////////////////////////////////////////////////
    PSCESVC_CONFIGURATION_INFO     pConfigInfo = NULL;
    SCESTATUS                      retCode;
    SCE_ENUMERATION_CONTEXT        EnumContext = 0;
  
  

    if ( pSceCbInfo == NULL ||
         pSceCbInfo->sceHandle == NULL ||
         pSceCbInfo->pfQueryInfo == NULL ||
         pSceCbInfo->pfSetInfo == NULL ||
         pSceCbInfo->pfFreeInfo == NULL ) 
    {
        return(SCESTATUS_INVALID_PARAMETER);
    }


  ////////////////////////////////////////////////////
  // Retrieve information from security database.
  ///////////////////////////////////////////////////
    do
    {
        retCode =  (*(pSceCbInfo->pfQueryInfo))(
                              pSceCbInfo->sceHandle,
                              SceSvcConfigurationInfo,
                              NULL,
                              FALSE,
                              &pConfigInfo,
                              &EnumContext
                              );
        if(retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
        {
          ULONG i;
          for(i = 0;i < pConfigInfo->Count; i++)
          {
            if(pConfigInfo->Line[I].Key == NULL) 
                continue;
        
        //////////////////////////////////////////////
        // Query service for corresponding key.
        //////////////////////////////////////////////
            QueryConfigurationLine(
                               pConfigInfo->Line[i].Key,
                               &SystemValue);
        
        //////////////////////////////////////////////
        // Compare values.
        //////////////////////////////////////////////
            CompareValue(
                     pConfigInfo->Line[i].Key,
                     SystemValue,
                     pConfigInfo->Line[i].Value,
                     &Result);
        
        //////////////////////////////////////////////
        // Write to security database if values are 
        // not equal.
        //////////////////////////////////////////////
            if(Result != NULL)
            {
              retCode =  (*(pSceCbInfo->pfSetInfo))(pSceCbInfo->sceHandle,
                                      SceSvcAnalysisInfo,
                                      pConfigInfo->Line[i].Key,
                                      TRUE,
                                      Result);
              if(retCode != SCESTATUS_SUCCESS)
              {
                //////////////////////////////////////////
                // Add code to handle other return codes.
                //////////////////////////////////////////
              }
            }
        }
      
          //////////////////////////////////////////////
          // Free all buffers used to retrieve 
          // SceSvcFree frees memory allocated by call 
          // to SceSvcQueryQueryInfo. 
          /////////////////////////////////////////
        (*(pSceCbInfo->pfFreeInfo)) (PVOID)pConfigInfo);
          pConfigInfo = NULL;
    }
  } while (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL);
  
  
  //////////////////////////////////////////////////
  // If the return code is not SCESTATUS_SUCCESS, add code to 
  // set error message appropriately.
  //////////////////////////////////////////////////
  return retCode;
}
```



 

 



