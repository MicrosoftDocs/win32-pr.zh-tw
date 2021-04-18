---
title: 搭配 Exchange 使用 ADSI
description: 若為 Exchange 2000，將 ADSI 與 Exchange 搭配使用的資訊包含在 Exchange 2000 SDK 中。 如需詳細資訊，請參閱 ADSI 的管理工作。
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- ADSI for Exchange ADSI
- ADSI for Exchange ADSI，信箱
- ADSI for Exchange ADSI、信箱、建立
- ADSI for Exchange ADSI、信箱、刪除
- ADSI for Exchange ADSI、信箱、設定安全描述項
- ADSI for Exchange ADSI、信箱、尋找 home server for
- ADSI for Exchange ADSI，取得和修改訊息
- ADSI for Exchange ADSI，安全描述項
- ADSI for Exchange ADSI、安全描述項、操作
- ADSI for Exchange ADSI，安全描述項，設定
- ADSI for Exchange ADSI，收件者容器
- ADSI for Exchange ADSI，查看 Exchange 物件屬性
- ADSI for Exchange ADSI、接收者容器、自訂
- ADSI for Exchange ADSI，Exchange Server
- ADSI for Exchange ADSI、Exchange Server、流覽和修改架構
- ADSI for Exchange ADSI、Exchange Server、清單伺服器版本
- ADSI for Exchange ADSI、Exchange Server、組織和網站名稱
- ADSI for Exchange ADSI、Exchange Server、尋找信箱首頁伺服器
- ADSI for Exchange ADSI，電子郵件地址，正在抓取
- ADSI for Exchange ADSI、通訊群組清單、建立
- ADSI for Exchange ADSI、隱藏或刪除的專案
- ADSI for Exchange ADSI，正在取得目錄服務變更
- ADSI for Exchange ADSI，訊息大小
- ADSI for Exchange ADSI，疑難排解問題
- 信箱 ADSI
- 信箱 ADSI，建立
- 信箱 ADSI，刪除
- 信箱 ADSI，設定安全描述項
- 信箱： ADSI，尋找 home server
- 訊息 ADSI、取得和修改
- Exchange ADSI
- Exchange ADSI，信箱
- Exchange ADSI，信箱，建立
- Exchange ADSI，信箱，刪除
- Exchange ADSI，信箱，設定安全描述項于
- Exchange ADSI、信箱、尋找 home server
- Exchange ADSI，取得和修改訊息
- Exchange ADSI，安全描述項
- Exchange ADSI，安全描述項，操作
- Exchange ADSI，安全描述項，設定
- Exchange ADSI，收件者容器
- Exchange ADSI，查看 Exchange 物件屬性
- Exchange ADSI，收件者容器，自訂
- Exchange ADSI、Exchange Server
- Exchange ADSI、Exchange Server、流覽和修改架構
- Exchange ADSI、Exchange Server、清單伺服器版本
- Exchange ADSI、Exchange Server、組織和網站名稱
- Exchange ADSI、Exchange Server、尋找信箱首頁伺服器
- Exchange ADSI，電子郵件地址，正在抓取
- Exchange ADSI，通訊群組清單，建立
- Exchange ADSI、隱藏或刪除的專案
- Exchange ADSI，正在進行目錄服務變更
- Exchange ADSI，訊息大小
- Exchange ADSI，疑難排解問題
- 適用于 Exchange 物件的安全描述項 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833d60c284a12e759eb74b22c9aa48abc75da463
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106968720"
---
# <a name="using-adsi-with-exchange"></a>搭配 Exchange 使用 ADSI

若為 Exchange 2000，將 ADSI 與 Exchange 搭配使用的資訊包含在 Exchange 2000 SDK 中。 如需詳細資訊，請參閱 [ADSI 的管理](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65))工作。

您可以在本節中找到下列工作：

-   建立使用者 URL
-   建立 Active Directory 路徑
-   使用 ADSI 列舉 Exchange 2000 伺服器
-   使用 ADSI 操控擴充屬性
-   使用 ADSI 新增/移除管理員物件
-   使用 ADSI/ADO 列舉 Exchange 物件屬性
-   使用 ADSI 抓取舊版 Exchange 辨別名稱
-   使用 ADSI 尋找 Exchange 組織名稱
-   使用 ADSI 尋找 Exchange 通訊清單
-   使用 CDOEXM 和 ADSI 建立通訊群組清單
-   使用 ADSI 在 SMTP 虛擬伺服器上設定訊息限制

若為 Exchange 5.5，adsi 參考和使用資訊可在 [Adsi Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80)) 指南中找到。

您可以在本節中找到下列工作：

-   查看和修改 Exchange Server 架構
-   查看 Exchange 物件的原始屬性
-   建立 Exchange 信箱
-   設定 Exchange 信箱上的安全描述項
-   操作安全描述項和 Sid
-   刪除信箱物件
-   建立自訂的收件者
-   建立收件者容器
-   從伺服器取得組織和網站名稱
-   列出組織中所有伺服器的 Exchange server 版本
-   尋找信箱的主伺服器
-   正在抓取電子郵件地址
-   存取隱藏或刪除的專案
-   正在抓取對目錄服務所做的變更
-   從查詢結果建立通訊群組清單
-   取得或修改訊息大小
-   使用 LDAP 錯誤碼針對問題進行疑難排解

 

 