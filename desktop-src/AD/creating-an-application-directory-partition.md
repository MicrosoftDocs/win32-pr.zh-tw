---
title: 建立應用程式目錄分割
description: 應用程式目錄分割是由 domainDNS 物件代表，其 instanceType 屬性值為 DS \_ instanceType \_ \_ \_ 。 nc HEAD 與 ds instanceType nc 的組合 \_ \_ \_ 是可 \_ 寫入的。
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- 建立應用程式目錄分割廣告
- 應用程式目錄分割廣告，建立
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a17471696825179b6e49230b5168abbaf88b8e2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462897"
---
# <a name="creating-an-application-directory-partition"></a>建立應用程式目錄分割

應用程式目錄分割是由 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) 物件代表，其 [**instanceType**](/windows/desktop/ADSchema/a-instancetype) 屬性值為 **ds InstanceType。 \_ \_ \_ nc \_ HEAD** 與 **ds instanceType nc 的組合 \_ \_ \_ 是可 \_ 寫入** 的。 這個 **domainDNS** 物件代表應用程式目錄分割根目錄 (NC head) ，其命名類似一般網域分割區，例如 "DC = DYNAMICDATA，DC = FABRIKAM，DC = com"，其對應至 DNS 名稱 "dynamicdata.fabrikam.com"。 因此，應用程式目錄分割可以在可具現化網域分割區的任何地方具現化。 沒有與應用程式目錄分割相關聯的 NetBIOS 名稱。

您可以嵌套應用程式目錄分割，也就是應用程式目錄分割可以有子應用程式目錄分割。 使用根目錄在應用程式目錄分割前端之子樹範圍的搜尋，將會產生子應用程式目錄分割的接續參考。

只有當 Windows Server 2003 和更新版本的網域控制站持有 Domain-Naming FSMO 角色時，才能在 Windows Server 2003 和更新版本上執行的網域控制站上建立應用程式目錄分割複本。 在同時具有 Windows Server 2003 網域控制站和下層網域控制站 (Windows 2000 網域控制站或 Windows NT 4.0 網域主控站) 的混合樹系中，嘗試在下層網域控制站上建立應用程式目錄分割複本將會失敗。

應用程式目錄分割在設定分割區的分割區容器中也有對應的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。 您可以在建立 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns)物件之前，手動預先建立 **交叉引用**。 預先建立的 **交叉引用** 物件必須具有下表所示的屬性值，否則資料分割建立將會失敗。 如果 **交叉引用** 物件不存在，則在建立應用程式目錄分割時，Active Directory 伺服器會建立一個。

| 屬性                          | 描述                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | 包含將建立應用程式目錄分割之網域控制站的 DNS 路徑。                               |
| [**啟用**](/windows/desktop/ADSchema/a-enabled) | 包含 **FALSE**。                                                                                                                       |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | 包含分割區的分辨名稱。 在上述範例中，此屬性會包含 "DC = dynamicdata，DC = mydomain，DC = com"。 |



 

**若要使用其第一個複本建立新的應用程式目錄分割，請執行下列步驟**

1.  系結至新磁碟分割的命名空間，並指定將在 ADsPath 中裝載應用程式目錄分割的網域控制站。 例如，若要建立具有 ADsPath "DC = dynamicdata，DC = mydomain，DC = com" 的分割區，系結 ADsPath 會是 "LDAP:// <domain controller> /DC = mydomain，dc = com"，其中 " &lt; domain controller &gt; " 是將裝載分割區之網域控制站的 DNS 名稱。

    系結作業必須指定 [快速] 和 [委派] 選項。 [快速] 選項可讓系結成功，即使命名空間不存在也一樣。 需要委派選項，才能讓網域控制站使用相同的認證來與 Domain-Naming FSMO 角色持有者聯繫。

    網域控制站的系統版本必須是 Windows Server 2003 作業系統和更新版本。

2.  使用適當的資料分割名稱建立 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) 物件，例如 "DC = dynamicdata"，以代表新分割區的命名內容標頭。 **DomainDNS** 物件必須具有值為5的 [**instanceType**](/windows/desktop/ADSchema/a-instancetype)屬性 (**DS \_ instanceType \_ 是 \_ nc \_** 前端 \| **ds \_ instanceType \_ nc \_ 是可 \_ 寫入的**) 。 **InstanceType** 屬性只能在建立時設定，因為它是僅限系統的屬性。

建立 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) 物件時，Active Directory 伺服器將執行下列步驟：

1.  搜尋分割區容器中具有與分割區辨別名稱相符的 [**nCName**](/windows/desktop/ADSchema/a-ncname)屬性值的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件，如果找到相符的專案，則修改 **交叉引用** 物件以代表應用程式目錄分割。 如果找不到相符的 **交叉引用** 物件，Active Directory 伺服器會建立新的 **交叉引用** 物件，以代表應用程式目錄分割。

    下表列出 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件的重要屬性。

    | 屬性                                                              | 描述                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**nCName**](/windows/desktop/ADSchema/a-ncname)                                       | 包含分割區的分辨名稱。                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | 包含資料分割的 DNS 名稱。                                                                                                            |
    | [**高階 NC-複本-位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | 第一個複本之網域控制站的 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) 物件的辨別名稱會新增至此屬性。 |

    

     

2.  起始設定分割區的同步處理，並等候完成。 這可讓用戶端應用程式在系結至用來建立應用程式目錄分割的相同網域控制站時，修改新建立的應用程式目錄分割的設定參數。
3.  使用 DS INSTANCETYPE 建立 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) 物件 **\_ \_ 是 \_ NC \_ HEAD** ， **ds \_ INSTANCETYPE \_ NC 是 \_ \_** [**INSTANCETYPE**](/windows/desktop/ADSchema/a-instancetype) 屬性上設定的可寫入旗標。 **InstanceType** 屬性也可以包含其他私用旗標。
4.  使用新建立的應用程式目錄分割的辨別名稱，在目標網域控制站的 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa)物件中填入 [**nc 的 ms-chap**](/windows/desktop/ADSchema/a-msds-hasmasterncs)屬性。

當您建立應用程式目錄分割，或是新增並完全同步處理應用程式目錄分割的新複本時，Active Directory 伺服器會正確地向 NetLogon 和 DNS 註冊複本。 如需詳細資訊和已註冊的 SRV 記錄清單，請參閱 [尋找應用程式目錄磁碟分割主機伺服器](locating-an-application-directory-partition-host-server.md)。

如需建立應用程式目錄分割的詳細資訊，請參閱 [建立應用程式目錄分割的範例程式碼](example-code-for-creating-an-application-directory-partition.md)。

## <a name="locating-the-partitions-container"></a>尋找磁碟分割容器

您可以透過下列兩種方式之一來找到分割區容器的分辨名稱。 第一個是更複雜的執行，但一律會提供精確的結果：

1.  系結至 RootDSE 並取得 **configurationNamingCoNtext** 屬性。
2.  使用 **configurationNamingCoNtext** 屬性系結至設定容器。
3.  在 configuration 容器中搜尋屬於 [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) 類型的物件。
4.  取得 [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer)物件的 **distinguishedName** 屬性值。 這會是分割區容器的分辨名稱。

如需詳細資訊和示範此方法來尋找分割區容器的程式碼範例，請參閱尋找分割區 [容器的範例程式碼](example-code-for-locating-the-partitions-container.md)中的 **GetPartitionsDNSearch** 函數。

第二個方法比較簡單，但依賴具有特定相對辨別名稱的分割區容器。 目前不可能變更分割區容器的名稱，但如果未來加入這項功能，如果已重新命名分割區容器，則下列程式將無法正確運作。

1.  系結至 RootDSE 並取得 **configurationNamingCoNtext** 屬性。
2.  合併字串 "CN = 分割區"，後面接著 **configurationNamingCoNtext** 屬性，以形成分割區容器的分辨名稱。 辨別名稱的格式會是 "CN = 磁碟分割" <configuration DN> 。

如需詳細資訊和示範此方法來尋找分割區容器的程式碼範例，請參閱尋找分割區 [容器的範例程式碼](example-code-for-locating-the-partitions-container.md)中的 **GetPartitionsDNManual** 函數。

 

 