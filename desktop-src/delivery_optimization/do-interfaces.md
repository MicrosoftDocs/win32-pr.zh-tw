---
title: DO 介面
description: 使用下列傳遞最佳化 (執行) 介面，以傳輸檔案和監視傳送佇列中的作業。
ms.assetid: 20203CCD-86CC-4551-BA4F-0A5999F8C956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0359328f189c1a5b5d9649d8300dc59a80df4480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106967673"
---
# <a name="do-interfaces"></a>DO 介面

使用下列傳遞最佳化 (執行) 介面，以傳輸檔案和監視傳送佇列中的作業。

| 介面 | 描述 |
|-|-|
| [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) | 用戶端會執行 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面，以接收作業已完成、已修改或發生錯誤的通知。 |
| [**IBackgroundCopyError**](ibackgroundcopyerror.md) | 捕獲作業錯誤的詳細資料。 |
| [**IBackgroundCopyFile**](ibackgroundcopyfile.md) | 抓取作業中檔案傳輸要求的本機和遠端檔案名，以及其進度。 |
| [**IBackgroundCopyFile2**](ibackgroundcopyfile2.md) | 指定檔案的新遠端名稱，並抓取要下載的範圍清單。 |
| [**IBackgroundCopyFile5**](ibackgroundcopyfile5.md) | 提供 BackgroundCopyFile 屬性的泛型屬性 get 和 set 方法。 |
| [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) | 將檔案加入至作業、設定作業的優先權層級、判斷工作的狀態，以及啟動和停止作業。 |
| [**IBackgroundCopyJob5**](ibackgroundcopyjob5.md) | 查詢或設定工作的數個選擇性行為。 |
| [**IBackgroundCopyManager**](ibackgroundcopymanager.md) | 建立傳送作業、抓取佇列中作業的列舉值物件，以及從佇列中取出個別的作業。 |
| [**IDeliveryOptimizationJob**](ideliveryoptimizationjob.md) | 用來下載檔案的範圍。 |
| [**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md) | 用來識別特定檔案的狀態。 |
| [**IDODownload**](./do/nn-do-idodownload.md) | 用來啟動及管理下載。 |
| [**IDODownloadInternal**](./dodownloadinternal/nn-dodownloadinternal-idodownloadinternal.md) | 用來取得或設定擴充的下載屬性。 |
| [**IDODownloadStatusCallback**](./do/nn-do-idodownloadstatuscallback.md) | 用來接收有關下載的通知。 |
| [**IDOManager**](./do/nn-do-idomanager.md) | 用來建立新的下載，以及列舉現有的下載。 |
| [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) | 列舉作業中的檔案。 |