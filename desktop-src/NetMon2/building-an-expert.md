---
description: 本主題說明如何建立網路監視器 SDK 隨附的一般專家。
ms.assetid: c05b261d-3fac-40bf-b4ff-bd766f8d148f
title: 打造專家
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ead0ff222b72c66bfc88ec477d1a8d6a941273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192636"
---
# <a name="building-an-expert"></a>打造專家

本主題說明如何建立網路監視器 SDK 隨附的一般專家。

> [!Note]  
> 在建立下列程式碼範例之前，請先安裝網路監視器 SDK 並初始化 MySetEnv.bat 檔。

 

**打造一般專家**

1.  開啟網路監視器命令提示字元，然後流覽至 \\ 專家子目錄; 例如，C： \\ Program Files \\ NetMonSDK2 \\ 專家。
2.  輸入 **xcopy/e/s/V Blrplate MyExpert**;然後，在出現提示時，輸入 **D**。
3.  移至 \\ MyExpert 子目錄。
4.  輸入 **Ren Blrplate \* 。 \*MyExpert \* ... \*** 確定已正確地重新命名所有檔案。 藉由比較 \\ 專家 Blrplate 子目錄中的檔案來驗證檔案名 \\ 。
5.  使用 **MyExpert** 取代所有出現的 **Blrplate** ，以編輯 Makefile。
6.  使用 **MyExpert** 取代所有出現的 **Blrplate** ，以編輯 .cpp 檔案。 請注意，在 Config.xml 中的對話方塊識別碼必須是大寫 (例如， **MYEXPERT**) 。
7.  以 **MyExpert** 取代所有出現的 **Blrplate** ，以編輯 MyExpert。
8.  將 **BLRPLATE** 重新命名為 **MYEXPERT**，以編輯 Resrc1。  (記住， **MYEXPERT** 必須是大寫) 。
9.  將 [ **idd \_ BLRPLATE \_ config \_ ] 對話方塊** 重新命名為 [ **idd \_ MyExpert \_ config \_ ] 對話方塊**，以編輯 MyExpert .rc 檔。
10. 輸入 **nmake** 來建立 DLL 檔案。 若要驗證組建，請將目錄變更為 \\ Obj 子目錄，並確認該檔案存在。 如需詳細資訊，請參閱 [觀看專家 DLL 屬性](viewing-expert-dll-properties.md)。

當組建完成時，您將會有一個專家 DLL，您可以使用網路監視器進行測試和部署。 如需有關安裝專家的詳細資訊，請參閱 [安裝專家至網路監視器 2.1](installing-an-expert-to-network-monitor-2-1.md)。 如需有關如何偵測專家的詳細資訊，請參閱 [將專家進行調試](debugging-an-expert.md)。

 

 



