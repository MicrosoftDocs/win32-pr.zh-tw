---
description: 傳送至 view 回呼物件的通知，以指定應該註冊變更通知事件的位置和事件。
title: 'SFVM_GETNOTIFY 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193576"
---
# <a name="sfvm_getnotify-message"></a>SFVM \_ GETNOTIFY 訊息

傳送至 view 回呼物件的通知，以指定應該註冊變更通知事件的位置和事件。 註冊之後，在這些位置或事件上發生變更時，就會通知 view 回呼物件。 這些事件會透過 [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) 傳送至 view 回呼，然後由視圖處理。


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pidl* \[擴展\]
</dt> <dd>

專案之絕對 Idlist.txt 的指標，此專案應註冊以收到變更的通知。 一般來說，這與所要查看位置的 Idlist.txt 相同，但它可以是其他位置。

> [!IMPORTANT]
> 此值的存留期是由 view 回呼物件所擁有。 若不再需要，您必須負責建立 view 回呼物件，然後釋放此值。 這需要 view 回呼物件儲存這個值。 此值通常可以儲存在 view 回呼物件的 **\_ pidlMonitor** 成員中。 透過 *pidl* 所傳回之值的擁有權規則是非標準的，而且需要特別注意。 View 回呼物件必須擁有此值，並確保不會釋出視圖回呼物件本身。

 

</dd> <dt>

*lEvents* \[擴展\]
</dt> <dd>

值，其中包含一或多個 SHCNE 值。 如需可能值的清單，請參閱 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 。 當任何相關聯的事件發生時，view 回呼物件將會註冊以接收 [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) 訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

已忽略，但應該傳回 S \_ OK。

## <a name="remarks"></a>備註

如果此回呼訊息未針對 Idlist.txt 或事件遮罩傳回非零值，則此視圖將不會註冊變更通知。

## <a name="examples"></a>範例

下列範例顯示 **SFVM \_ GETNOTIFY** 的 view 回呼函式處理常式程式碼的範例執行。


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SFVM \_ QUERYFSNOTIFY**](sfvm-queryfsnotify.md)
</dt> <dt>

[**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
