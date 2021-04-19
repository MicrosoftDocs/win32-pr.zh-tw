---
description: Windows Installer 開發人員 Windows SDK 元件中提供 VBScript 程式碼範例檔案 WiTextIn.vbs。
ms.assetid: ba6c6367-ebb1-4981-ae3a-bcff68aacdbf
title: 將 ANSI 檔案複製到資料庫欄位
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc6c4d3a945177581a35bf6b19d89855abb5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974498"
---
# <a name="copy-ansi-file-into-a-database-field"></a>將 ANSI 檔案複製到資料庫欄位

[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供 VBScript 程式碼範例檔案 WiTextIn.vbs。 此範例會示範如何使用腳本，將檔案複製到 Windows Installer 資料庫的文字欄位中，並示範主鍵資料的處理方式。

程式碼範例也會顯示下列各項：

-   [**OpenDatabase 方法 (安裝程式物件)**](installer-opendatabase.md)和 [**安裝程式物件**](installer-object.md)的 [**LastErrorRecord 方法**](installer-lasterrorrecord.md)
-   [**OpenView 方法**](database-openview.md)、 [**Commit 方法**](database-commit.md)和 [**Database 物件**](database-object.md)的 [**PrimaryKeys 屬性**](database-primarykeys.md)
-   [**View 物件**](view-object.md)的 [**Fetch 方法**](view-fetch.md)和 [**Modify 方法**](view-modify.md)
-   [**Record 物件**](record-object.md)的 [**至 convertfrom-stringdata 屬性**](record-stringdata.md)和 [**ReadStream 方法**](record-readstream.md)

若要使用程式碼範例，您需要 Windows Script Host 的 CScript.exe 或 WScript.exe 版本。

**使用 CScript.exe 來執行此範例**

-   在命令提示字元中，輸入下列語法：

    **cscript WiTextIn.vbs \[ 路徑指向資料庫 \] \[ 資料表名稱 \] \[ 主鍵值的資料 \] \[ 行名稱 \] \[ 路徑\]**

> [!Note]  
> 如果第一個引數是/？，則會顯示說明 或者，如果指定的引數太少。

 

**將輸出重新導向至檔案**

-   以下列： **VBS > 檔案路徑結束命令列 \[ \] 。T**

> [!Note]  
> 此範例會傳回值 0 (零) 表示成功，1 (一個) （如果叫用說明），而如果腳本失敗，則為 2 (兩個) 。

 

下列清單會識別您必須指定的專案：

-   指定 Windows Installer 資料庫的路徑。
-   指定資料庫資料表的名稱。
-   依序指定資料列的所有主要索引鍵值，並以冒號串連。
-   請指定不是索引鍵資料行的資料行名稱。 這是您想要接收資料的資料行。
-   指定要複製之文字檔的路徑。

> [!Note]  
> 如果省略最後一個引數，則會顯示欄位中目前的值。

 

如需其他腳本範例，請參閱 [Windows Installer 腳本範例](windows-installer-scripting-examples.md)。 如需不需要 Windows Script Host 的範例公用程式，請參閱 [Windows Installer 開發工具](windows-installer-development-tools.md)。

 

 



