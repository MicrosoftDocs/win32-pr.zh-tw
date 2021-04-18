---
title: 變更使用者資訊的元素
description: 網路管理功能可提供各種不同的資訊層級，以協助變更使用者資訊。
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966039"
---
# <a name="changing-elements-of-user-information"></a>變更使用者資訊的元素

網路管理功能可提供各種不同的資訊層級，以協助變更使用者資訊。 某些層級需要系統管理許可權才能順利執行。 如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。

本主題中的範例程式碼示範如何藉由呼叫 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數來變更使用者資訊的數個元素。 此程式碼會使用各種網路管理資訊結構。

變更使用者資訊時，最好是使用該資訊的特定層級。 這可防止在使用較低層級值時意外重設不相關的資訊。

下列程式碼範例說明如何設定一些較常用的層級：

-   [設定使用者密碼，層級1003](#setting-the-user-password-level-1003)
-   [設定使用者權限，層級1005](#setting-the-user-privilege-level-1005)
-   [設定使用者主目錄，層級1006](#setting-the-user-home-directory-level-1006)
-   [設定使用者批註欄位，層級1007](#setting-the-user-comment-field-level-1007)
-   [設定使用者旗標，層級1008](#setting-the-user-flags-level-1008)
-   [設定使用者腳本路徑，層級1009](#setting-the-user-script-path-level-1009)
-   [設定使用者授權單位旗標，層級1010](#setting-the-user-authority-flags-level-1010)
-   [設定使用者的完整名稱，層級1011](#setting-the-user-full-name-level-1011)

所有程式碼片段都假設使用者已定義 UNICODE compile 指示詞，並包含適當的 SDK 標頭檔，如下所示：


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

#define SERVER L"test_server_name"
#define USERNAME L"test_user_name"

DWORD netRet = 0;
```



## <a name="setting-the-user-password-level-1003"></a>設定使用者密碼，層級1003

下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式的呼叫，將使用者的密碼設定為已知的值。 [**使用者 \_ 資訊 \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)主題包含其他資訊。


```C++
#define PASSWORD L"new_password"

USER_INFO_1003 usriSetPassword;
//
// Set the usri1003_password member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriSetPassword.usri1003_password = PASSWORD;
    
netRet = NetUserSetInfo( SERVER, USERNAME, 1003, (LPBYTE)&usriSetPassword, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1003!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1003\n", netRet);
```



## <a name="setting-the-user-privilege-level-1005"></a>設定使用者權限，層級1005

下列程式碼片段說明如何使用對 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式的呼叫，來指定指派給使用者的許可權層級。 [**使用者 \_ 資訊 \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)主題包含其他資訊。 如需帳戶許可權的詳細資訊，請參閱 [許可權](/windows/desktop/SecAuthZ/privileges) 和 [授權常數](/windows/desktop/SecAuthZ/authorization-constants)。


```C++
USER_INFO_1005 usriPriv;
//
// Set the usri1005_priv member to the appropriate value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriPriv.usri1005_priv = USER_PRIV_USER;

netRet = NetUserSetInfo( SERVER, USERNAME, 1005, (LPBYTE)&usriPriv, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1005!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1005\n", netRet);
```



## <a name="setting-the-user-home-directory-level-1006"></a>設定使用者主目錄，層級1006

下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式的呼叫來指定使用者主目錄的路徑。 目錄可以是硬式編碼的路徑或有效的 Unicode 路徑。 [**使用者 \_ 資訊 \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)主題包含其他資訊。


```C++
#define HOMEDIR L"C:\\USER\USER_PATH"
USER_INFO_1006 usriHomeDir;
//
// Set the usri1006_home_dir member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriHomeDir.usri1006_home_dir = HOMEDIR;

netRet = NetUserSetInfo( SERVER, USERNAME, 1006, (LPBYTE)&usriHomeDir, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1006!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1006\n", netRet);
```



## <a name="setting-the-user-comment-field-level-1007"></a>設定使用者批註欄位，層級1007

下列程式碼片段說明如何藉由呼叫 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式來建立批註與使用者之間的關聯。 [**使用者 \_ 資訊 \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)主題包含其他資訊。


```C++
#define COMMENT L"This is my Comment Text for the user"
USER_INFO_1007 usriComment;
//
// Set the usri1007_comment member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriComment.usri1007_comment = COMMENT;

netRet = NetUserSetInfo( SERVER, USERNAME, 1007, (LPBYTE)&usriComment, NULL );

if( netRet == NERR_Success )
    printf("Success with level 1007!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1007\n", netRet);
```



## <a name="setting-the-user-flags-level-1008"></a>設定使用者旗標，層級1008

下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數的呼叫來設定使用者旗標。 「 [**使用者 \_ 資訊 \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) 」主題包含旗標的有效值清單以及每個旗標的描述。

請注意，您 \_ 必須針對 Windows NT、windows 2000、WINDOWS XP 和 LAN Manager 網路設定 UF 腳本旗標。 嘗試設定其他旗標而不 \_ 在這些網路上設定 UF 腳本，將會導致 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數失敗。


```C++
#define USR_FLAGS UF_SCRIPT | UF_NORMAL_ACCOUNT
USER_INFO_1008 usriFlags;
//
// Set the usri1008_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFlags.usri1008_flags = USR_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1008, (LPBYTE)&usriFlags, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1008!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1008\n", netRet);
```



## <a name="setting-the-user-script-path-level-1009"></a>設定使用者腳本路徑，層級1009

下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數的呼叫來設定特定使用者的登入腳本檔案的路徑。 腳本檔案可以是。CMD 檔案、。EXE 檔案或。.BAT 檔案。 字串也可以是 null。 [**使用者 \_ 資訊 \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)主題包含其他資訊。


```C++
#define SCRIPT_PATH L"C:\\BIN\\MYSCRIPT.BAT"
USER_INFO_1009 usriScrPath;
//
// Set the usri1009_script_path member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriScrPath.usri1009_script_path = SCRIPT_PATH;
netRet = NetUserSetInfo( SERVER, USERNAME, 1009, (LPBYTE)&usriScrPath, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1009!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1009\n", netRet);
```



## <a name="setting-the-user-authority-flags-level-1010"></a>設定使用者授權單位旗標，層級1010

下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函式的呼叫來設定使用者的操作員許可權旗標。 「 [**使用者 \_ 資訊 \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) 」主題包含旗標的有效值清單以及每個旗標的描述。


```C++
#define AUTHORITY_FLAGS AF_OP_ACCOUNTS
USER_INFO_1010 usriAuthFlags;
//
// Set the usri1010_auth_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriAuthFlags.usri1010_auth_flags = AUTHORITY_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1010, (LPBYTE)&usriAuthFlags, NULL);
if( netRet == NERR_Success )
    printf("Success with level 1010!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1010\n", netRet);
```



## <a name="setting-the-user-full-name-level-1011"></a>設定使用者的完整名稱，層級1011

下列程式碼片段說明如何使用 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數的呼叫來設定使用者的完整名稱。 [**使用者 \_ 資訊 \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)主題包含其他資訊。


```C++
#define USER_FULL_NAME L"Joe B. User"
USER_INFO_1011 usriFullName;
//
// Set the usri1011_full_name member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFullName.usri1011_full_name = USER_FULL_NAME;
netRet = NetUserSetInfo( SERVER, USERNAME, 1011, (LPBYTE)&usriFullName, NULL);
if( netRet == NERR_Success ) 
    printf("Success with level 1011!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo\n", netRet);
```



 

 