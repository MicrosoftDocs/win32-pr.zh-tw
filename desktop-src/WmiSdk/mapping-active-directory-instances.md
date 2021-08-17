---
description: 一般而言，每個 Active Directory 物件都只會對應到一個 WMI 實例。
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Active Directory 實例的對應
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a3e40a6f4a85ebb1bb3d7e1e5a5de7bc43c754ff7672f694aff05b62853dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317635"
---
# <a name="mapping-active-directory-instances"></a>Active Directory 實例的對應

一般而言，每個 Active Directory 物件都只會對應到一個 WMI 實例。 對應至 WMI 實例的 WMI 類別，與對應的 Active Directory 類別中的類別提供者所提供的類別相同。 每個實例的索引鍵屬性 **ADSIPath** 會填入物件的 ADSI 路徑。

本主題將討論下列各節：

-   [對應命名空間](#mapping-namespaces)
-   [對應屬性值](#mapping-attribute-values)
-   [對應實例關聯](#mapping-instance-associations)

> [!Note]  
> 如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。

 

## <a name="mapping-namespaces"></a>對應命名空間

ADSI 中的每個命名空間都會對應至 WMI \\ 根目錄命名空間中的命名空間 \\ 。 WMI 命名空間的名稱與提供命名空間之目錄服務提供者的 **ProgId** 值相同。 具體來說，Active Directory 對應至 \\ \\ 根目錄命名空間中的 LDAP 命名空間 \\ 。 WMI 會在 \\ 類別提供者註冊過程中建立 LDAP 命名空間。

## <a name="mapping-attribute-values"></a>對應屬性值

下表列出 Active Directory 物件的每個屬性與 WMI 屬性之間的對應。



| Active Directory 語法 | WMI 資料類型                                 | WMI 屬性值                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| Boolean                 | **CIM \_ 布林值**                              | 直接對應至適當的布林值。                         |
| 不區分大小寫的字串 | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| 區分大小寫的字串   | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| 辨別名稱      | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| DN-Binary               | **\_ 具有 \_ 二進位** 之類別 DN 的内嵌物件 | 對應至 **\_ 具有 \_ 字串** 類別之 DN 的實例。                    |
| DN-String               | **\_ 具有 \_ 字串** 之類別 DN 的内嵌物件 | 對應至 **\_ 具有 \_ 字串** 類別之 DN 的實例。                    |
| 列舉型別             | **CIM \_ SINT32**                               | 直接對應至整數值。                                     |
| IA5-String              | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| 整數                 | **CIM \_ SINT32**                               | 直接對應至整數值。                                     |
| NT 安全描述項  | **Uint8Array** 類別的内嵌物件       | 對應至 **Uint8Array** 類別的實例。                          |
| 數值字串          | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| 物件識別碼               | **CIM \_ 字串**                               | 從 OID 的字串表示進行對應;例如，"1.3.3.4"。 |
| 八位字串            | **Uint8Array** 類別的内嵌物件       | 對應至 **Uint8Array** 類別的實例。                          |
| 或名稱                 | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| Presentation-Address    | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| 列印案例字串       | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| 複本連結            | **Uint8Array** 類別的内嵌物件       | 對應至 **Uint8Array** 類別的實例。                          |
| SID                     | **Uint8Array** 類別的内嵌物件       | 對應至 **Uint8Array** 類別的實例。                          |
| 時間                    | **CIM \_ DATETIME**                             | 轉換成 CIM \_ DATETIME 標記法並對應。                 |
| 未定義               | N/A                                           | N/A                                                                       |
| Unicode 字串          | **CIM \_ 字串**                               | 從字串的值對應。                                      |
| UTC 編碼時間          | **CIM \_ DATETIME**                             | 轉換成 CIM \_ DATETIME 標記法並對應。                 |



 

如需有關 **\_ 使用 \_ 二進位** **Uint8Array** 和 DN 的詳細資訊，請參閱 [對應屬性](mapping-active-directory-classes.md)。

## <a name="mapping-instance-associations"></a>對應實例關聯

目錄服務提供者會使用 [**DS \_ LDAP \_ 實例 \_**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment) 內含專案類別的實例，在 Active Directory 中對應不同的容器關聯性。

 

 
