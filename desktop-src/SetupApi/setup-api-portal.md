---
description: 從具有設定腳本和 inf 檔案的程式安裝設備磁碟機。 撰寫安裝程式以進行裝置設定和驅動程式安裝。 基於安裝軟體應用程式的目的，不再建議使用此 api。
ms.assetid: 96a9e472-9b92-4976-9379-dc0c96524963
title: 設定 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101c2673e72095d0cf4ebe59c1cece83449d647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980314"
---
# <a name="setup-api"></a>設定 API

## <a name="purpose"></a>目的

安裝程式 API 會提供一組功能，讓安裝應用程式呼叫來執行安裝作業。

## <a name="where-applicable"></a>適用時

您可以使用這些安裝程式來開發安裝應用程式。 安裝程式 API 不應再用來安裝應用程式。 相反地，請使用 [Windows Installer](/windows/desktop/Msi/windows-installer-portal)開發應用程式安裝程式。 安裝程式 API 會繼續用來安裝設備磁碟機。

安裝程式 API 適用于桌面樣式應用程式的開發。

## <a name="developer-audience"></a>開發人員對象

如果開發人員的安裝應用程式需要下列功能，則可以使用安裝程式 API：

-   檔案的佇列。
-   檔案的安裝。
-   處理安裝錯誤和提示媒體的程式。
-   正在更新登錄專案。
-   記錄檔安裝時進行記錄。
-   最近使用的來源路徑的儲存體。

## <a name="run-time-requirements"></a>執行階段需求求

如需哪些作業系統需要哪些作業系統才能使用特定功能的相關資訊，請參閱函式檔集的需求一節。

## <a name="in-this-section"></a>本節內容



| 主題                                 | 描述                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| [概觀](overview.md)<br/>   | 有關安裝程式 API 的一般資訊。<br/>                                             |
| [參考](reference.md)<br/> | 安裝程式 API 資料類型、結構、函數和通知的檔。<br/> |



 

 

