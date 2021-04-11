---
description: 針對在上一節中建立的五個範例自訂動作，輸入 CustomAction 資料表的記錄。 如需有關如何為這種類型的自訂動作填入 CustomAction 資料表的詳細資訊，請參閱自訂動作類型1。
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: 撰寫 CustomAction 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944005"
---
# <a name="authoring-the-customaction-table"></a>撰寫 CustomAction 資料表

針對在上一節中建立的五個範例自訂動作，輸入 [CustomAction 資料表](customaction-table.md)的記錄。 如需有關如何為這種類型的自訂動作填入 CustomAction 資料表的詳細資訊，請參閱 [自訂動作類型 1](custom-action-type-1.md)。

[CustomAction 資料表](customaction-table.md)



| 動作            | 類型  | 來源      | 目標                |
|-------------------|-------|-------------|-----------------------|
| ProcessAccounts   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

Windows Installer SDK 提供動態連結程式庫的 c + + 原始程式碼。 使用進程 .cpp 來建立檔案 Process.dll。 使用 Create .cpp Create.dll 建立檔案。 您可以使用 Remove .cpp 來建立 Remove.dll。 將這些動態連結程式庫檔案新增至二進位資料表。

[二進位資料表](binary-table.md)



| Name        | 資料            |
|-------------|-----------------|
| Process.dll | {*二進位資料*} |
| Create.dll  | {*二進位資料*} |
| Remove.dll  | {*二進位資料*} |



 

繼續 [新增自訂 CustomUserAccounts 資料表](adding-a-custom-customuseraccounts-table.md)。

 

 



