---
description: HKLM \\ SOFTWARE \\ Microsoft \\ MSSQLServer \\ Client。
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025893"
---
# <a name="connectto"></a>ConnectTo

**HKLM \\ SOFTWARE \\ Microsoft \\ MSSQLServer \\ 用戶端**

## <a name="description"></a>Description

**ConnectTo** 子機碼會儲存連接至 Microsoft SQL Server database engine 實例之以 Windows 為基礎的用戶端的連接資訊。 此子機碼中的登錄專案屬於資料類型 REG \_ SZ，而其值會指定要用來連接到實例的 Net-Library，以及任何網路特定的參數。

此子機碼中儲存的連接資訊是由 SQL Server、SQL Server ODBC 驅動程式或 SQL Server DB-Library 動態連結程式庫 (DLL) 的 OLE DB 提供者讀取。

## <a name="change-method"></a>變更方法

您不應該使用 [登錄編輯程式] 來修改此子機碼中的專案。 使用 SQL Server 用戶端網路公用程式來設定伺服器名稱和連接資訊。 如需進一步指示，請參閱 SQL Server 用戶端網路公用程式說明。

## <a name="notes"></a>備註

-   OLE DB 提供者會使用 **ConnectTo** 子機碼來 SQL Server、SQL Server ODBC 驅動程式和 SQL SERVER DB-Library DLL。 此子機碼中的專案會識別 Net-Library 這些資料存取應用程式開發介面 (API) 元件呼叫的專案。
-   Net-Libraries 是保護資料存取 API 元件的 SQL Server 元件，從使用不同的處理序間通訊 (IPC) 方法的詳細資料，到與 SQL Server 資料庫引擎的 instancess 通訊。
-   不當更新 **ConnectTo** 子機碼可能會導致應用程式無法順利連接到 SQL Server database engine 的實例。

 

 



