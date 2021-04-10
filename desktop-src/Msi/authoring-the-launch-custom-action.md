---
description: 名為啟動的範例自訂動作的原始程式碼（符合範例規格）是由 Windows Installer SDK 提供，以做為檔案教學課程 .cpp。
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: 撰寫啟動自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944003"
---
# <a name="authoring-the-launch-custom-action"></a>撰寫啟動自訂動作

名為啟動的範例自訂動作的原始程式碼（符合範例規格）是由 Windows Installer SDK 提供，以做為檔案教學課程 .cpp。 此自訂動作會使用 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) 將包含屬性的字串格式化。 屬性 \[ \# FileKey 會 \] 解析為 HTML 檔案的完整路徑。 使用來源檔案建立 Tutorial.dll 的檔案。 此 DLL 的進入點為 LaunchTutorial。

範例自訂動作啟動會呼叫以 c + + 撰寫的 DLL，並從暫存二進位資料流程產生。 此類型的自訂動作包括基底類型常數 msidbCustomActionTypeDll 和 msidbCustomActionTypeBinaryData，其提供等於1的基底數數值型別。 請參閱 [自訂動作類型 1](custom-action-type-1.md)。 因為規格需要在自訂動作失敗時繼續安裝，所以啟動也會包含選用的常數 **msidbCustomActionTypeContinue**，也就是64。 請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。 啟動的總數字類型為65。

繼續將 [啟動新增至 CustomAction 和二進位資料表](adding-launch-to-the-customaction-and-binary-tables.md)。

 

 



