---
description: InstallAdminPackage 動作會將產品資料庫複製到 TARGETDIR 屬性所定義的系統管理安裝點。
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: InstallAdminPackage 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943992"
---
# <a name="installadminpackage-action"></a>InstallAdminPackage 動作

InstallAdminPackage 動作會將產品資料庫複製到 [**TARGETDIR**](targetdir.md) 屬性所定義的系統管理安裝點。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                                 |
|-------|------------------------------------------------------------|
| \[1\] | 安裝檔案的名稱。                                     |
| \[6\] | 資料庫的大小。                                          |
| \[9\] | 系統管理安裝–點目錄的識別碼。 |



 

## <a name="remarks"></a>備註

InstallAdminPackage 動作也會更新資料庫的摘要資訊，並在複製資料庫之後，移除任何位於資料流程中的封包檔。

 

 



