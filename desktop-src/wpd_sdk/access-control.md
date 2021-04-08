---
description: 存取控制
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: " (WPD API) 的存取控制"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852156"
---
# <a name="access-control-wpd-api"></a> (WPD API) 的存取控制

Windows Driver Model (WDM) 支援在) 隨插即用 PnP (裝置節點上，透過存取控制清單來限制裝置存取 (Acl) 。 這表示廠商和網路系統管理員可以限制對任何裝置類型的存取。 當應用程式透過呼叫 [**IPortableDevice：： Open 開啟**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)驅動程式的控制碼時，驅動程式的 i/o 管理員會驗證指定的使用者是否具有必要的存取權，而且當 IOCTLs 從該控制碼傳送至驅動程式時，也會有同樣的存取檢查。

例如，網路系統管理員可以將來賓使用者限制為可存取可攜式裝置的唯讀存取權，並將其授與已驗證的使用者讀取/寫入存取權。 在此情況下，這表示如果來賓發出需要讀取/寫入存取權的 WPD 命令 (例如刪除物件) ;它會因為拒絕存取而失敗，而如果已驗證的使用者發出相同的命令，則會成功。

用來控制卸除式存放裝置和可攜式裝置存取權的群組原則專案，其實不是讓系統管理員輕鬆地將 PnP 裝置節點 Acl 套用到整個裝置類別的方法 (例如，套用「拒絕可攜式裝置的寫入權限」群組原則會調整所有 WPD 裝置的 Acl，以拒絕) 的寫入存取權。

## <a name="io-control-codes-in-wpd"></a>WPD 中的 i/o 控制碼

WPD 應用程式會藉由開啟裝置控制碼和傳送 i/o 控制項碼 (IOCTLs) 來與驅動程式進行通訊。 這些 IOCTLs 包含四個區段：

1.  裝置類型
2.  函數代碼
3.  Buffer 方法
4.  存取類型

第四個區段（存取類型）指定給定命令的特定存取需求。 驅動程式的 i/o 管理員會使用此資料來執行 (ACL) 檢查的存取控制清單。

如果將 IOCTL 定義為：


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



驅動程式的 i/o 管理員會在傳送此訊息時，檢查裝置控制碼的擁有者是否具有裝置的讀取存取權。

而且，如果將 IOCTL 定義為：


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



當傳送此訊息時，驅動程式的 i/o 管理員會檢查裝置控制碼的擁有者是否具有裝置的讀取/寫入存取權。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式總覽**](application-overview.md)
</dt> <dt>

[**IPortableDevice：： Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



