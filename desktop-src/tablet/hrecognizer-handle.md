---
description: HRECOGNIZER 控制碼可用來建立辨識器內容、取出辨識器的屬性和屬性，以及判斷辨識器需要哪些封包屬性來執行辨識。
ms.assetid: 1fc1901e-8c4d-4ef1-8c38-52d46ce10a48
title: 'HRECOGNIZER 控制碼 (Recapis .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e78086ff86453ef8b0157bb3b274f3c47be0dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318475"
---
# <a name="hrecognizer-handle"></a>HRECOGNIZER 控制碼

**HRECOGNIZER** 控制碼可用來建立辨識器內容、取出辨識器的屬性和屬性，以及判斷辨識器需要哪些封包屬性來執行辨識。


```C++
typedef HANDLE HRECOGNIZER;
```



## <a name="remarks"></a>備註

下列函數使用 **HRECOGNIZER**。



| 函式                                                               | 描述                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**CreateRecognizer**](/windows/desktop/api/recapis/nf-recapis-createrecognizer)                           | 建立辨識器。<br/>                                                                   |
| [**DestroyRecognizer**](/windows/desktop/api/recapis/nf-recapis-destroyrecognizer)                         | 終結辨識器。<br/>                                                                  |
| [**GetRecoAttributes**](/windows/desktop/api/recapis/nf-recapis-getrecoattributes)                         | 傳回辨識器的屬性。<br/>                                               |
| [**CreateCoNtext**](/windows/desktop/api/recapis/nf-recapis-createcontext)                                 | 建立辨識器內容。<br/>                                                           |
| [**DestroyCoNtext**](/windows/desktop/api/recapis/nf-recapis-destroycontext)                               | 終結辨識器內容。<br/>                                                          |
| [**GetAllRecognizers**](/windows/desktop/api/recapis/nf-recapis-getallrecognizers)                         | 取得所有辨識器。<br/>                                                                   |
| [**GetResultPropertyList**](/windows/desktop/api/recapis/nf-recapis-getresultpropertylist)                 | 抓取辨識器可針對結果範圍傳回的屬性清單。<br/>            |
| [**GetPreferredPacketDescription**](/windows/desktop/api/recapis/nf-recapis-getpreferredpacketdescription) | 抓取包含辨識器所使用之封包屬性的封包描述。<br/> |
| [**GetUnicodeRanges**](/windows/desktop/api/recapis/nf-recapis-getunicoderanges)                           | 抓取辨識器支援的 Unicode 點範圍。<br/>                    |
| [**LoadCachedAttributes**](/windows/desktop/api/recapis/nf-recapis-loadcachedattributes)                   | 載入辨識器的快取屬性。<br/>                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                        |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>Recapis。h</dt> </dl> |



 

 




