---
description: InstallAdminPackage 動作會將產品資料庫複製到 TARGETDIR 屬性所定義的系統管理安裝點。
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: InstallAdminPackage 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1879d711e1a52a7121326ba170bb3a004fbfb4ee988b35d19a16e1a53c3e2811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996588"
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

 

 



