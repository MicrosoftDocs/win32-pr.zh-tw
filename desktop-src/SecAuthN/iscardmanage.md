---
description: 用來連接到特定的智慧卡或讀取器，以建立其他選用的介面來執行特定的智慧卡功能、鎖定特定的智慧卡以進行獨佔使用，以及取得智慧卡或讀取器的狀態。
ms.assetid: 67077034-5bd0-4176-9dc7-774caba3d427
title: ISCardManage 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage
api_type:
- COM
api_location: ''
ms.openlocfilehash: cce31ea21701c098b09a0bd96360afb374a9bccc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194503"
---
# <a name="iscardmanage-interface"></a>ISCardManage 介面

\[**ISCardManage** 介面不再適用于 windows server 2008、windows Vista 及 windows Server 2003 Service Pack 1 (SP1) 和更新版本。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

下列介面定義是以標準的形式提供，可在開發 [*智慧卡*](../secgloss/s-gly.md)[*服務提供者*](../secgloss/c-gly.md)時遵循。

必須提供 **ISCardManage** 介面。 它是用來連接到特定的 [*智慧卡*](../secgloss/s-gly.md) 或 [*讀取器*](../secgloss/r-gly.md)，以建立其他選用的介面來執行特定的智慧卡功能、鎖定特定的智慧卡以進行獨佔使用，以及取得智慧卡或讀者的狀態。 作為一組，這些服務可以負責維護妥善定義的內容，讓應用程式可以與 [*智慧卡*](../secgloss/s-gly.md) 或 [*讀者*](../secgloss/r-gly.md)進行通訊。

以下是 **ISCardManage** 介面的一般用法。

**連接到智慧卡**

1.  建立與卡片相關聯的 **ISCardManage** 介面。
2.  連接到特定智慧卡讀卡機 ([**AttachByIFD**](iscardmanage-attachbyifd.md)) 或使用先前取得的控制碼 ([**AttachByHandle**](iscardmanage-attachbyhandle.md)) ，以連接到智慧卡。
3.  建立其他介面來執行智慧卡作業 ([**CreateCardAuth**](iscardmanage-createcardauth.md)、 [**CreateFileAccess**](iscardmanage-createfileaccess.md)、 [**CreateCHVerification**](iscardmanage-createchverification.md)或 [**CreateInterface**](iscardmanage-createinterface.md)) 。
4.  釋放卡片 (卸 [**離**](iscardmanage-detach.md)) 。
5.  視需要釋放 **ISCardManage** 介面和其他專案。

## <a name="members"></a>成員

**ISCardManage** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardManage** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISCardManage** 介面具有這些方法。



| 方法                                                            | 描述                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachByHandle**](iscardmanage-attachbyhandle.md)             | 允許應用程式使用智慧卡 [*資源管理員*](../secgloss/r-gly.md)所傳回的控制碼，建立智慧卡的通訊連結。<br/>                                              |
| [**AttachByIFD**](iscardmanage-attachbyifd.md)                   | 允許應用程式要求建立以顯示名稱參考之特定讀取器的內容。<br/>                                                                                                                                               |
| [**CreateCardAuth**](iscardmanage-createcardauth.md)             | 允許建立 [**ISCardAuth**](iscardauth.md) 介面。<br/>                                                                                                                                                                                            |
| [**CreateCHVerification**](iscardmanage-createchverification.md) | 允許建立 [**ISCardVerify**](iscardverify.md) 介面。<br/>                                                                                                                                                                                        |
| [**CreateFileAccess**](iscardmanage-createfileaccess.md)         | 允許建立 [**ISCardFileAccess**](iscardfileaccess.md) 介面。<br/>                                                                                                                                                                                |
| [**CreateInterface**](iscardmanage-createinterface.md)           | 允許建立介面。<br/>                                                                                                                                                                                                                            |
| [**中斷連結**](iscardmanage-detach.md)                             | 分別釋放 [**AttachByHandle**](iscardmanage-attachbyhandle.md) 或 [**AttachByIFD**](iscardmanage-attachbyifd.md) 所配置的特定智慧卡或讀取器的附件。<br/>                                                                |
| [**重新連接**](iscardmanage-reconnect.md)                       | 允許應用程式重新連線到智慧卡或讀取器，而不需要分別發出卸 [**離**](iscardmanage-detach.md) 、 [**AttachByHandle**](iscardmanage-attachbyhandle.md) 或 [**AttachByIFD**](iscardmanage-attachbyifd.md) 。<br/> |
| [**SCardLock**](iscardmanage-scardlock.md)                       | 鎖定連線的智慧卡或讀取器以供獨佔使用。<br/>                                                                                                                                                                                                       |
| [**SCardUnlock**](iscardmanage-scardunlock.md)                   | 釋出連線智慧卡或讀取器的專用用途。<br/>                                                                                                                                                                                                   |
| [**狀態**](iscardmanage-status.md)                             | 允許應用程式取得智慧卡或讀取器的目前狀態。<br/>                                                                                                                                                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



 

 
