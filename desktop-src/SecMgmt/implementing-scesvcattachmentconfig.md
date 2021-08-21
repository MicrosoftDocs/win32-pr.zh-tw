---
description: 必須從安全性資料庫取出資訊，然後使用該資訊來設定服務。
ms.assetid: c0c1c1e4-de5b-405d-abe8-33a985ce98e5
title: 執行 SceSvcAttachmentConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2eef460184773b4b09bed3ae36c88ae5854bc001cb9437aaaccce66231838eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969305"
---
# <a name="implementing-scesvcattachmentconfig"></a>執行 SceSvcAttachmentConfig

[**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)函數必須從安全性資料庫取出資訊，然後使用該資訊來設定服務。

在執行 [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)時，您可以取出所有資訊，然後設定服務，或是在步驟中取得和設定服務。 下列演算法會抓取所有資訊，然後設定服務。

**若要執行 SceSvcAttachmentConfig**

1.  定義取出資訊和傳回碼所需的變數。
2.  在回呼結構中呼叫 pfQueryInfo 回呼函式，以從安全性資料庫中取出設定資訊。
3.  使用傳回的資訊來設定系統。
4.  在回呼結構中呼叫 pfFreeInfo 回呼函式，以釋放用於傳回之資訊的記憶體。
5.  如果有任何訊息要將擴充功能新增至分析記錄檔，請在回呼結構中呼叫 pfLogInfo 回呼函式。
6.  傳回適當的 **SCESTATUS** 碼。

下列範例顯示一個可能的 [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)執行。 請注意，在此範例中，函數 ProcessConfigurationLine 會設定服務設定。 未顯示此函式的實作為。


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig (
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
      // Retrieve configuration information and configure
      // system. 
      ////////////////////////////////////////////////////
      do
      {
            retCode = (*(pSceCbInfo->pfQueryInfo))( pSceCbInfo->sceHandle,
                                  SceSvcConfigurationInfo,
                                  NULL,
                                  FALSE,
                                  (PVOID *)&pConfigInfo,
                                  &EnumContext
                                 );
            if (retCode == SCESTATUS_SUCCESS && pConfigInfo != NULL)
            {
              ULONG i:
              //////////////////////////////////////////////////
              // Configure system.
              /////////////////////////////////////////////////
              for(i = 0; < pConfigInfo->Count; i++)
              {
                if(pConfigInfo->Line[i].Key == NULL) 
                    continue;
                ProcessConfigurationLine(pConfigInfo->Line[i]);
              }
      
      
              //////////////////////////////////////////////////
              // Free data returned.
              /////////////////////////////////////////////////
              (*(pSceCbInfo->pfFreeInfo)) ((PVOPID)pConfigInfo);
              pConfigInfo = NULL;
            }
        } while (retCode == SCESTATUS_SUCCESS && CountReturned > 0);
  
  
  ////////////////////////////////////////////////////
  // Add code for other return codes if retCode is 
  // not SCESTATUS_SUCCESS.
  ///////////////////////////////////////////////////
  return retCode;
}
```



 

 



