---
description: 下列介面定義是以標準的形式提供，可在開發智慧卡服務提供者時遵循。
ms.assetid: 68cc0bbe-ce8e-4da1-b907-596caa95a39c
title: ISCardFileAccess 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess
api_type:
- COM
api_location: ''
ms.openlocfilehash: fcfcdc75bcf10b922a242574bfabe267c949fa52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850143"
---
# <a name="iscardfileaccess-interface"></a>ISCardFileAccess 介面

\[**ISCardFileAccess** 介面可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

下列介面定義是以標準的形式提供，可在開發 [*智慧卡*](../secgloss/s-gly.md)[*服務提供者*](../secgloss/c-gly.md)時遵循。

**ISCardFileAccess** 介面可用來根據 ISO/IEC 7816-4 中定義的結構，使用基礎卡片檔案系統來對卡片型檔案系統執行高階介面。 其他實作為可能，但這應該是最常見的。

**ISCardFileAccess** 介面可用來以對電腦環境中應用程式開發人員非常熟悉的方式來公開檔案系統實體。 它提供了尋找特定檔案和執行一般作業（例如選取、讀取、寫入、建立和刪除）的機制。 它會封裝和遮罩大部分的低層級詳細資料，包括在卡片層級執行這些作業。

以下是 **ISCardFileAccess** 介面的一般用法。 在此情況下， **ISCardFileAccess** 介面是用來選取、開啟和寫入檔案。

**寫入檔案**

1.  呼叫 [**ISCardManage：： CreateFileAccess**](iscardmanage-createfileaccess.md) 來建立 **ISCardFileAccess** 介面。
2.  呼叫 [**Open**](iscardfileaccess-open.md) 以選取並開啟檔案。
3.  呼叫 [**Write**](iscardfileaccess-write.md)。
4.  呼叫 [**Close**](iscardfileaccess-close.md)。
5.  釋放 **ISCardFileAccess** 介面。

## <a name="members"></a>成員

**ISCardFileAccess** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **ISCardFileAccess** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ISCardFileAccess** 介面具有這些方法。



| 方法                                                              | 描述                                                                                                                                  |
|:--------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeDir**](iscardfileaccess-changedir.md)                     | 將目前的智慧卡目錄變更為新指定的目錄。<br/>                                                          |
| [**關閉**](iscardfileaccess-close.md)                             | 關閉指定的檔案。<br/>                                                                                                        |
| [**建立**](iscardfileaccess-create.md)                           | 在 ICC 檔案系統內的指定位置建立檔案。<br/>                                                                    |
| [**刪除**](iscardfileaccess-delete.md)                           | 刪除指定的檔案。<br/>                                                                                                         |
| [**目錄**](iscardfileaccess-directory.md)                     | 抓取檔案清單。<br/>                                                                                                        |
| [**GetCurrentDir**](iscardfileaccess-getcurrentdir.md)             | 傳回目前所選目錄的絕對路徑。<br/>                                                                     |
| [**GetFileCapabilities**](iscardfileaccess-getfilecapabilities.md) | 捕獲檔案功能。<br/>                                                                                                      |
| [**GetProperties**](iscardfileaccess-getproperties.md)             | 取得指定之物件的標記所參考的基本資料。<br/>                                                           |
| [**無效**](iscardfileaccess-invalidate.md)                   | 使指定的檔案無效。<br/>                                                                                               |
| [**打開**](iscardfileaccess-open.md)                               | 開啟指定的檔案以供進一步使用。<br/>                                                                                         |
| [**讀**](iscardfileaccess-read.md)                               | 從指定的檔案讀取並傳回指定的資料。<br/>                                                                           |
| [**恢復**](iscardfileaccess-rehabilitate.md)               | 使用不正確命令（可由應用程式存取），使檔案 (EF 或 DF) 。<br/> |
| [**Seek**](iscardfileaccess-seek.md)                               | 選取將完成讀取/寫入權限的物件。<br/>                                                                 |
| [**SetProperties**](iscardfileaccess-setproperties.md)             | 設定指定之物件的標記所參考的基本資料。<br/>                                                                |
| [**寫**](iscardfileaccess-write.md)                             | 將資料寫入目前開啟的檔案。<br/>                                                                                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



 

 
