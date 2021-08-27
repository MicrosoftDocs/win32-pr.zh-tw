---
title: 使用 ADSI 搭配 Exchange
description: 針對 Exchange 2000，在 Exchange 2000 SDK 中包含使用 ADSI 搭配 Exchange 的資訊。 如需詳細資訊，請參閱 ADSI 的管理工作。
ms.assetid: c806ca1b-c97c-4567-af8b-e12cfde2bf70
ms.tgt_platform: multiple
keywords:
- adsi for Exchange adsi
- adsi for Exchange adsi，信箱
- adsi for Exchange adsi、信箱、建立
- adsi for Exchange adsi、信箱、刪除
- adsi for Exchange adsi、信箱、設定安全描述項
- adsi for Exchange adsi、信箱、尋找 home server for
- adsi for Exchange adsi、取得和修改訊息
- adsi for Exchange adsi，安全描述項
- adsi for Exchange adsi、安全描述項、操作
- adsi for Exchange adsi、安全描述項、設定
- adsi for Exchange adsi，收件者容器
- adsi for Exchange adsi，查看 Exchange 物件屬性
- adsi for Exchange adsi、收件者容器、自訂
- adsi for Exchange adsi，Exchange Server
- adsi for Exchange adsi、Exchange Server、觀看和修改架構
- adsi for Exchange adsi、Exchange Server、清單伺服器版本
- adsi for Exchange adsi、Exchange Server、組織和網站名稱
- adsi for Exchange adsi、Exchange Server、尋找信箱首頁伺服器
- adsi for Exchange adsi，電子郵件地址，正在抓取
- adsi for Exchange adsi、通訊群組清單、建立
- adsi for Exchange adsi、隱藏或刪除的專案
- adsi for Exchange adsi，正在取得目錄服務變更
- adsi for Exchange adsi，訊息大小
- adsi for Exchange adsi，疑難排解問題
- 信箱 ADSI
- 信箱 ADSI，建立
- 信箱 ADSI，刪除
- 信箱 ADSI，設定安全描述項
- 信箱： ADSI，尋找 home server
- 訊息 ADSI、取得和修改
- Exchange編輯器
- ExchangeADSI、信箱
- ExchangeADSI、信箱、建立
- ExchangeADSI、信箱、刪除
- ExchangeADSI、信箱、設定安全描述項
- ExchangeADSI、信箱、尋找 home server
- ExchangeADSI、取得和修改訊息
- ExchangeADSI、安全描述項
- ExchangeADSI、安全描述項、操作
- ExchangeADSI、安全描述項、設定
- ExchangeADSI、收件者容器
- ExchangeADSI，觀看 Exchange 物件屬性
- ExchangeADSI、收件者容器、自訂
- ExchangeADSI、Exchange Server
- ExchangeADSI、Exchange Server、觀看和修改架構
- ExchangeADSI、Exchange Server、清單伺服器版本
- ExchangeADSI、Exchange Server、組織和網站名稱
- ExchangeADSI，Exchange Server，尋找信箱首頁伺服器
- ExchangeADSI，電子郵件地址，正在抓取
- ExchangeADSI、通訊群組清單、建立
- ExchangeADSI、隱藏或刪除的專案
- ExchangeADSI，正在抓取目錄服務變更
- ExchangeADSI、訊息大小
- ExchangeADSI，疑難排解問題
- Exchange 物件的安全描述項 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f48a1015674ea8bf413cb9edbf55f0f64f6211b85bb876baeb6ab47868482ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690127"
---
# <a name="using-adsi-with-exchange"></a>使用 ADSI 搭配 Exchange

針對 Exchange 2000，在 Exchange 2000 SDK 中包含使用 ADSI 搭配 Exchange 的資訊。 如需詳細資訊，請參閱 [ADSI 的管理](/previous-versions/office/developer/exchange-server-2003/aa125368(v=exchg.65))工作。

您可以在本節中找到下列工作：

-   建立使用者 URL
-   建立 Active Directory 路徑
-   使用 ADSI 列舉 Exchange 2000 伺服器
-   使用 ADSI 操控擴充屬性
-   使用 ADSI 新增/移除管理員物件
-   使用 ADSI/ADO 列舉 Exchange 物件屬性
-   使用 ADSI 抓取舊版 Exchange 辨別名稱
-   使用 ADSI 尋找 Exchange 的組織名稱
-   使用 ADSI 尋找 Exchange 通訊清單
-   使用 CDOEXM 和 ADSI 建立通訊群組清單
-   使用 ADSI 在 SMTP 虛擬伺服器上設定訊息限制

針對 Exchange 5.5，adsi [Exchange](/previous-versions/office/developer/exchange-server-2007/aa579394(v=exchg.80))指南中可以找到 adsi 參考和使用資訊。

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
-   列出組織中所有伺服器的 Exchange 伺服器版本
-   尋找信箱的主伺服器
-   正在抓取電子郵件地址
-   存取隱藏或刪除的專案
-   正在抓取對目錄服務所做的變更
-   從查詢結果建立通訊群組清單
-   取得或修改訊息大小
-   使用 LDAP 錯誤碼針對問題進行疑難排解

 

 